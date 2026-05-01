# Agent Tool Requirements Reference

Each skill in this graph needs a concrete answer to: "What tools, APIs, and credentials do I need to actually execute this?" This reference defines the standard options so skills can point here instead of reinventing execution paths.

## Capability Tiers

### Tier 1 — Agent-Executable (Automated)
Skills that can run entirely via agent tools without manual platform interaction:
- **web_search**: Firecrawl search, DuckDuckGo, Bing API
- **web_extract / web_scrape**: Firecrawl scrape, curl, browser_navigate + snapshot
- **browser_navigate + browser_snapshot**: For pages behind auth or JS rendering
- **terminal + curl**: Direct API calls with bearer tokens or API keys
- **execute_code / Python**: Data processing, CSV parsing, metric calculations

### Tier 2 — Human-Assisted (Manual)
Skills that require manual platform interaction or auth flows agents can't complete:
- Logging into social platforms (2FA, CAPTCHA)
- Pulling native analytics exports (requires clicking through platform UIs)
- DM access (requires logged-in session on mobile or web)
- TikTok/Instagram API access (heavily restricted, approval-required)

## Tool Options per Platform

### X (Twitter)
| Method | Tool | Auth Required | Notes |
|--------|------|--------------|-------|
| X API v2 (Free) | `curl` + Bearer token | X_BEARER_TOKEN from developer portal | 1,500 tweets/month POST, 100 GET/15min |
| X API v2 (Basic) | `curl` + Bearer token | $100/month | 3,000 tweets/month POST, 10,000 GET/month |
| Browser (read-only) | `browser_navigate` → `browser_snapshot` | Logged-in session cookie | No posting, good for trending/monitoring |
| Trends24 | `browser_navigate` → trends24.in | None | Trending topics snapshot |
| Nitter (public instances) | `curl` or `browser_navigate` | None | Read-only, no auth, may be blocked |

### LinkedIn
| Method | Tool | Auth Required | Notes |
|--------|------|--------------|-------|
| LinkedIn API (Company pages) | `curl` + OAuth 2.0 | LINKEDIN_ACCESS_TOKEN + company page admin | Posting to company pages only |
| LinkedIn API (Member) | `curl` + OAuth 2.0 | LINKEDIN_ACCESS_TOKEN + member auth | Profile reads, limited |
| Browser (read-only) | `browser_navigate` → `browser_snapshot` | Logged-in session cookie | Profile viewing, post reading |
| Firecrawl search | `firecrawl search "site:linkedin.com/in/ ..."` | FIRECRAWL_API_KEY | Best for finding profiles |
| Firecrawl scrape | `firecrawl scrape URL` | FIRECRAWL_API_KEY | Extracting public profile/public post data |

### Instagram
| Method | Tool | Auth Required | Notes |
|--------|------|--------------|-------|
| Instagram Basic Display | `curl` + access token | INSTAGRAM_ACCESS_TOKEN | Read own media only |
| Instagram Graph API | `curl` + access token | Business/Creator account + Facebook page linked | Professional account analytics |
| Browser (read-only) | `browser_navigate` → `browser_snapshot` | Logged-in session cookie | Best for public profile reading |
| Firecrawl search | `firecrawl search "site:instagram.com/ ..."` | FIRECRAWL_API_KEY | Finding Instagram accounts |

### TikTok
| Method | Tool | Auth Required | Notes |
|--------|------|--------------|-------|
| TikTok Research API | `curl` + access token | TIKTOK_ACCESS_TOKEN (research account) | Public data only, restricted to researchers |
| TikTok Business API | `curl` + access token | TIKTOK_ACCESS_TOKEN (business account) | Own account analytics only |
| Browser (read-only) | `browser_navigate` → `browser_snapshot` | None (public profiles) | Best for viewing public TikTok profiles |
| Firecrawl search | `firecrawl search "site:tiktok.com/@ ..."` | FIRECRAWL_API_KEY | Finding TikTok accounts |

### Publishing Tools (Third-Party)
| Method | Tool | Auth Required | Notes |
|--------|------|--------------|-------|
| Buffer API | `curl` + access token | BUFFER_ACCESS_TOKEN | Queue posts across platforms |
| Hootsuite API | `curl` + OAuth | HOOTSUITE_ACCESS_TOKEN | Enterprise publishing |
| Typefully | Browser | Logged-in session | X thread scheduling |

## Environment Variables Reference

Create a `.env` or export these before running skills:

```bash
# Required for Tier 1 execution
export FIRECRAWL_API_KEY="fc-..."           # Website scraping and search
export X_BEARER_TOKEN="AAAAAAAA..."          # X API v2 (free tier)

# Optional — enables more platforms/features
export LINKEDIN_ACCESS_TOKEN="..."           # LinkedIn API
export INSTAGRAM_ACCESS_TOKEN="..."          # Instagram Graph API
export BUFFER_ACCESS_TOKEN="..."             # Buffer publishing
```

## When a Skill Cannot Execute

If a skill requires Tier 2 capabilities but the agent only has Tier 1 tools:
1. Flag the limitation explicitly in output
2. Do the maximum possible with available tools
3. Provide clear handoff instructions for the human
4. Mark remaining work as `needs_human`

## Skill Frontmatter Convention

Add to every skill:

```yaml
execution_tier: 1  # or 2
required_tools: [web_search, web_extract]  # from this reference
required_env_vars: [FIRECRAWL_API_KEY, X_BEARER_TOKEN]
fallback_if_unavailable: "Use browser_navigate to X.com/explore/tabs/trending instead of API"
```
