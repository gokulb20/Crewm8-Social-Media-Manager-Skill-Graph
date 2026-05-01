---
name: social-profile-discover
description: Discover social media profiles for a person or company using search engines, platform-specific searches, and website extraction — returns canonical profile URLs across LinkedIn, X, Instagram, Facebook, TikTok, and YouTube.
version: 1.0.0
author: Hermes (hermes-agent.nousresearch.com)
maintainer: Gokul (github.com/gokulb20)
license: MIT
homepage: https://crewm8.ai
tags: [social, research, discovery, profiles, linkedin, instagram, x, facebook]
related_skills: [prospect-social-audit, profile-audit]
inputs_required: [name, company-or-context, search-scope]
deliverables: [canonical-profile-urls-by-platform]
compatible_agents: [hermes, claude-code, droid, cursor, windsurf, openai, openclaw, generic]
execution_tier: 1
required_tools: [web_search, web_extract]
required_env_vars: [FIRECRAWL_API_KEY]
glossary_terms: []
---

# Social Profile Discover

Systematically discover social media profiles for a person or company. The output feeds directly into `prospect-social-audit` for evaluation and CRM enrichment.

## Purpose

Finding social profiles manually is inefficient and error-prone. This skill runs structured searches across platforms, extracts canonical profile URLs, and separates company profiles from personal profiles — so downstream skills get clean, verified data.

## When to Use

- Before running `prospect-social-audit` on a new company
- Enriching a CRM contact with their social presence
- Finding where a competitor or peer is active
- Building a target account list for social engagement
- Verifying that a discovered profile is actually the right person/company

## Inputs Required

- **Name** (person name or company name — required)
- **Company or context** (for disambiguation — "this person works at X")
- **Website** (optional — the best source of social links is the company's own footer)
- **Location** (optional — helps disambiguate common names)
- **Target platforms** (default: all — LinkedIn, X, Instagram, Facebook, TikTok, YouTube)

## Procedure

### Step 1: Check the website first

The company's own website is the most reliable source. Social icon links are usually in the footer, header, or Contact page.

```bash
firecrawl scrape "{website}" --format markdown
```

Extract all social URLs from `href` attributes:
- `linkedin.com/company/{slug}`
- `linkedin.com/in/{slug}` (personal)
- `instagram.com/{handle}`
- `facebook.com/{page}`
- `x.com/{handle}` or `twitter.com/{handle}`
- `tiktok.com/@{handle}`
- `youtube.com/@{handle}` or `youtube.com/channel/{id}`

### Step 2: Search per platform

For each platform not found on the website, search systematically:

**LinkedIn (person):**
```bash
firecrawl search "site:linkedin.com/in \"{name}\" {company} {title}" --limit 5
```

**LinkedIn (company):**
```bash
firecrawl search "site:linkedin.com/company \"{company_name}\" {location}" --limit 5
```

**X / Twitter:**
```bash
firecrawl search "site:x.com OR site:twitter.com \"{name}\" {company}" --limit 5
```

**Instagram:**
```bash
firecrawl search "site:instagram.com \"{company_name}\" {location}" --limit 5
```

**Facebook (business page):**
```bash
firecrawl search "site:facebook.com \"{company_name}\" {location}" --limit 5
```

**TikTok:**
```bash
firecrawl search "site:tiktok.com \"{name_or_company}\"" --limit 5
```

**YouTube:**
```bash
firecrawl search "site:youtube.com \"{company_name}\" channel" --limit 5
```

### Step 3: Verify each candidate profile

For each potential profile match, verify:

1. **Name match**: does the display name contain the expected name/company?
2. **Bio/description match**: does the bio mention the expected industry, location, or company?
3. **Activity match**: is the profile recently active (posts in last 90 days)?
4. **Follower match**: is the follower count plausible for this person/company?

Firecrawl scrape the profile page to extract bio and recent activity:

```bash
# For LinkedIn profiles (may return limited data for non-public profiles)
firecrawl scrape "{profile_url}" --format markdown

# For Instagram
firecrawl scrape "{instagram_url}" --format markdown

# For X
firecrawl scrape "{x_url}" --format markdown
```

### Step 4: Distinguish company vs. personal profiles

| Profile Type | Indicators |
|-------------|-----------|
| Company page | Multiple employees listed, "company" in URL, industry description |
| Personal profile | Single person, job titles, "in" in LinkedIn URL, individual posts |
| Creator/business account | Individual posting as a brand, often solo founders |

### Step 5: Compile canonical URLs

Return exactly one canonical URL per platform per entity (company vs person), or "Not found." Prefer:
- Website footer links > platform search results > search engine results
- Verified matches > unverified candidates
- Active profiles > dormant profiles

## Output Format

```markdown
# Social Profile Discovery: {Name}

## Source Summary
- **Website checked:** {url} (socials found: {count})
- **Platforms searched:** {platforms}
- **Profiles found:** {found}/{total searched}

## Company Profiles
| Platform | URL | Verified? | Source |
|----------|-----|-----------|--------|
| LinkedIn | {url} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |
| Instagram | @{handle} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |
| X | @{handle} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |
| Facebook | {url} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |
| TikTok | @{handle} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |
| YouTube | {url} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |

## Person Profiles ({contact_name} — if sought)
| Platform | URL | Verified? | Source |
|----------|-----|-----------|--------|
| LinkedIn | {url} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |
| X | @{handle} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |
| Instagram | @{handle} or "Not found" | {Yes/Probable/Unverified} | {Website / Search} |

## Unverified Candidates (for manual review)
- {url} — {why unsure} — {recommendation}

## JSON Export (for CRM)
```json
{
  "companySocials": {
    "linkedin": "...",
    "facebook": "...",
    "instagram": "...",
    "twitter": "...",
    "youtube": "...",
    "tiktok": "..."
  },
  "contactSocials": {
    "linkedin": "...",
    "twitter": "...",
    "instagram": "..."
  }
}
```
```

## Done Criteria

The skill is complete when:
1. All target platforms are searched (or explicitly skipped)
2. Each found profile has a verification status (Yes/Probable/Unverified)
3. Company and personal profiles are clearly separated
4. JSON export is ready for CRM enrichment
5. Unverified candidates are listed with recommendations

## Pitfalls

- Assuming the first search result is correct (verify before accepting)
- Mixing company and personal profiles (LinkedIn URLs: /company/ vs /in/)
- Missing profiles because the handle doesn't match the company name (always check the website footer)
- Rate-limiting: Firecrawl and platform search may throttle (space searches out)
- Firecrawl sometimes returns limited Markdown from LinkedIn (restricted by auth walls)

## Verification

For each "Verified: Yes" profile URL, open the link. Does the profile clearly belong to the target person/company? If you hesitate, mark it as "Probable" or "Unverified."

## See Also

- **references/platform-specs.md** — character limits, aspect ratios, benchmarks
- **references/tool-requirements.md** — API auth options, tool paths per platform
- **skills/research/prospect-social-audit/SKILL.md** — evaluates discovered profiles
