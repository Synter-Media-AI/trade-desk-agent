# The Trade Desk MCP Starter Kit — Manage Programmatic Ads with AI

[![MCP Compatible](https://img.shields.io/badge/MCP-compatible-blue)](https://modelcontextprotocol.io)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Platform: The Trade Desk](https://img.shields.io/badge/Platform-The%20Trade%20Desk-00B140)](https://www.thetradedesk.com)

**Enterprise programmatic advertising — CTV, audio, display, native, and video — managed by AI.** Open this repo in Amp, Cursor, or VS Code and manage The Trade Desk campaigns across the open internet with AI agents that handle bid optimization, audience segments, and cross-channel reporting.

---

## Why The Trade Desk + AI?

The Trade Desk (TTD) is the largest independent demand-side platform, processing 13 million ad impressions per second across connected TV (CTV), audio, display, native, and video inventory. Unlike walled gardens (Google, Meta, Amazon), TTD operates on the open internet — your ads appear on premium publishers, streaming services, podcasts, and digital billboards.

TTD's killer feature is Unified ID 2.0 (UID2) — a cookieless identity solution that's becoming the industry standard as third-party cookies disappear. While other DSPs scramble for cookie alternatives, TTD built the replacement.

The platform is powerful but complex. Campaigns have a deep hierarchy (advertiser → campaign → ad group → creative), bid optimization requires understanding of supply paths, and reporting across CTV/audio/display needs careful interpretation.

**Best for:** Enterprise brands, agencies managing $100K+/month in programmatic, connected TV (CTV) advertising, omnichannel campaigns, cookieless audience targeting.

---

## Quick Start (30 Seconds)

### Amp / Cursor / VS Code (Copilot)

1. **Get a free API key** at [syntermedia.ai/developer](https://syntermedia.ai/developer)
2. **Set the key:**
   ```bash
   export SYNTER_API_KEY=syn_your_key_here
   ```
3. **Open this repo** in your editor
4. **Start chatting** — MCP tools are pre-configured in `.mcp.json`

### Claude Desktop

Copy `claude_desktop_config.json` to your Claude config directory and replace the API key:

- **macOS:** `~/Library/Application Support/Claude/claude_desktop_config.json`
- **Windows:** `%APPDATA%\Claude\claude_desktop_config.json`

---

## What You Can Do

| Capability | Example |
|-----------|---------|
| **CTV Campaigns** | "Launch a connected TV campaign on Roku, Hulu, and Peacock" |
| **Display Campaigns** | "Create a display campaign targeting tech decision-makers on premium publishers" |
| **Audio Ads** | "Set up Spotify and podcast pre-roll targeting commuters aged 25-44" |
| **Native Ads** | "Create native ad placements on news and lifestyle publisher sites" |
| **Audience Segments** | "Build an audience using UID2 and first-party data from my CRM" |
| **Bid Optimization** | "Optimize bids toward a $20 CPA using Koa™ AI" |
| **Supply Path Control** | "Only bid on direct publisher inventory — no resellers" |
| **Cross-Channel Reports** | "Show me which channels (CTV, display, audio) drive the most conversions" |
| **Budget Pacing** | "Is my $50,000 monthly campaign pacing evenly?" |
| **Frequency Caps** | "Cap household frequency to 2 CTV impressions per day" |

---

## Example Conversations

### 1. Connected TV (CTV) Campaign Launch

> **You:** I want to run TV ads but my budget is $15,000/month. Is CTV on The Trade Desk realistic?
>
> **Agent:** Absolutely — $15,000/month is a solid CTV budget on TTD. Here's what I'd build:
>
> **Campaign structure:**
> - **Channel:** CTV (connected TV only — not linear broadcast)
> - **Inventory:** Hulu, Peacock, Tubi, Pluto TV, local news apps via Roku/Fire TV
> - **Format:** 15-second and 30-second pre-roll spots
> - **Budget:** $15,000/month (~$500/day)
> - **CPM:** $18-28 (depending on targeting precision)
>
> **Targeting:**
> - Households with income $100K+ (TTD's deterministic household data)
> - In-market for your product category (via TTD's third-party data marketplace)
> - Geographic: Top 20 DMAs where you have distribution
> - Daypart: Prime time (7-11 PM) gets highest completion rates
>
> **Why CTV over traditional TV:**
> | Metric | Traditional TV | CTV on TTD |
> |---|---|---|
> | Minimum buy | $50K+ | $5K |
> | Targeting | Age/gender/DMA | Income, interests, purchase behavior |
> | Measurement | Nielsen estimates | Exact household reach, completion rate, website visits |
> | Frequency control | None | Per-household per-day caps |
>
> **Expected results:** 750K-1M completed views, 85-95% video completion rate (CTV viewers can't skip), measurable lift in website traffic and branded search.

### 2. Cookieless Strategy with UID2

> **You:** Third-party cookies are going away. How does TTD handle that?
>
> **Agent:** The Trade Desk built the solution: **Unified ID 2.0 (UID2)**. Here's how it works and what it means for your campaigns:
>
> **UID2 vs Cookies:**
> | Feature | Third-Party Cookies | UID2 |
> |---|---|---|
> | Cross-device | No (per browser) | Yes (per person) |
> | CTV/Audio | Doesn't work | Works natively |
> | User consent | Implicit | Explicit opt-in |
> | Publisher adoption | Declining | Growing (80%+ of premium publishers) |
> | Persistence | Days (clearing) | Months (email-based) |
>
> **Your migration plan:**
> 1. **Upload first-party data:** Your customer email list → UID2-encrypted IDs → targetable across all TTD inventory
> 2. **Publisher signals:** Premium publishers using UID2 pass deterministic user IDs — no cookies needed
> 3. **Contextual fallback:** For non-UID2 inventory, TTD's contextual intelligence targets based on page content
>
> **Action items:**
> - Upload your CRM email list (I can hash and submit to TTD)
> - Enable UID2 on your website (add the UID2 JavaScript SDK)
> - Set up first-party data segments for retargeting
>
> Your cookie-dependent targeting reach will drop ~30% as cookies disappear, but UID2 recovers most of it — especially on CTV and audio where cookies never worked anyway.

### 3. Supply Path Optimization (SPO)

> **You:** I feel like I'm overpaying for inventory. Are there cheaper ways to buy the same impressions?
>
> **Agent:** Probably yes. Let me analyze your supply paths...
>
> **Current supply path analysis:**
> | Path | Impressions | Avg CPM | Win Rate | Hops |
> |---|---|---|---|---|
> | Direct to Publisher | 340K | $6.20 | 42% | 1 |
> | Via SSP (PubMatic) | 890K | $8.40 | 31% | 2 |
> | Via SSP (Magnite) | 720K | $9.10 | 28% | 2 |
> | Via Reseller → SSP | 210K | $14.30 | 15% | 3+ |
>
> **Findings:**
> - You're paying $14.30 CPM on resold inventory that's available directly for $6.20. That's a 131% markup.
> - Direct publisher paths have the highest win rate (42%) and lowest CPM ($6.20)
> - Multi-hop reseller paths waste 56% of your bid in intermediary fees
>
> **Recommended changes:**
> 1. Block all 3+ hop supply paths (saves ~$3,000/month)
> 2. Prioritize direct publisher deals via PMP (Private Marketplace)
> 3. Allowlist PubMatic and Magnite as preferred SSPs (good balance of reach and price)
> 4. Remove 14 low-quality supply sources flagged by TTD's SPO scoring
>
> Expected savings: 18-22% reduction in effective CPM with no loss in reach quality.

### 4. Cross-Channel Attribution

> **You:** I'm running CTV, display, and audio. How do I know which channel is actually driving conversions?
>
> **Agent:** This is where TTD's cross-device graph shines. Let me pull your attribution report...
>
> **Last 30 days — Conversion paths:**
>
> | Path | Conversions | % of Total | Avg Days to Convert |
> |---|---|---|---|
> | CTV → Display → Convert | 142 | 34% | 4.2 days |
> | Display only → Convert | 98 | 23% | 1.8 days |
> | CTV only → Convert | 87 | 21% | 6.1 days |
> | Audio → Display → Convert | 52 | 12% | 3.4 days |
> | Audio → CTV → Display → Convert | 38 | 9% | 7.8 days |
>
> **Key insight:** CTV rarely converts directly (21% solo), but it's the **initiator** in 43% of multi-touch paths. People see your TV ad, then later click a display retargeting ad. If you cut CTV, your display conversions would likely drop 30-40%.
>
> **Budget recommendation:**
> - CTV: 40% of budget (awareness driver)
> - Display: 40% of budget (conversion driver)
> - Audio: 20% of budget (supplementary reach)
>
> Don't judge CTV on last-click attribution — it's an upper-funnel channel that feeds your conversion pipeline.

### 5. Private Marketplace (PMP) Deals

> **You:** What are PMP deals and should I use them?
>
> **Agent:** PMP (Private Marketplace) deals are pre-negotiated agreements between you and specific publishers. Instead of bidding in the open auction, you get preferred access to premium inventory at a fixed CPM.
>
> **When to use PMPs:**
> - Brand safety is critical (you control exactly where ads appear)
> - You want premium placements (homepage takeovers, above-the-fold)
> - You need guaranteed inventory for a product launch
> - Open auction CPMs are too volatile
>
> **Current PMP opportunities I can set up:**
> | Publisher | Format | Est. CPM | Min Commitment |
> |---|---|---|---|
> | NYTimes.com | Display | $12 | $5K/month |
> | ESPN.com | Video | $22 | $10K/month |
> | Hulu | CTV 30s | $28 | $15K/month |
> | Spotify | Audio 30s | $15 | $5K/month |
>
> **Pro tip:** PMPs typically cost 20-40% more than open auction, but the inventory quality and brand safety justify it. A NYT PMP deal at $12 CPM is a better buy than open auction at $8 CPM on an unknown site.

---

## The Trade Desk Tips from the Pros

1. **CTV is the fastest-growing channel.** Connected TV ad spend is growing 30%+ annually. Costs are still reasonable ($15-28 CPM) compared to linear TV ($25-45 CPM). Get in now.
2. **Use UID2 for cookieless targeting.** Upload your first-party email list to create UID2-based segments. This provides cross-device, cross-channel targeting without cookies.
3. **Supply path optimization saves 15-25%.** Audit your supply paths quarterly. Direct publisher connections and preferred SSPs deliver better pricing and quality than multi-hop reseller chains.
4. **Don't judge CTV on last-click.** CTV is an awareness channel — it initiates conversion paths that display and search complete. Use TTD's multi-touch attribution to see the full picture.
5. **Frequency caps are per-household on CTV.** Unlike display where you cap per device, CTV caps are per household. Set 2-3 impressions per household per day.
6. **Koa™ AI handles bid optimization.** TTD's Koa engine processes 13M impressions/second. Let it optimize bids — manual bid management at this scale is impossible.
7. **Start with $10K/month minimum.** TTD's platform works best with meaningful data volume. Below $10K/month, the algorithm doesn't have enough signal to optimize effectively.

---

## FAQ

### Is there an MCP for The Trade Desk?
Yes — this repo. It pre-configures the Synter MCP server for TTD campaign management. Works with Amp, Cursor, VS Code, and Claude Desktop.

### What's the minimum spend for The Trade Desk?
TTD itself has no minimum, but their managed service agreements typically start at $25K-50K/month. Self-serve access is available through certified partners. The Synter MCP works with any TTD account.

### Can TTD run connected TV (CTV) ads?
Yes — CTV is TTD's strongest channel. Access Hulu, Peacock, Tubi, Pluto TV, Roku, Fire TV, and thousands of streaming apps. Full household-level targeting and measurement.

### What is UID2?
Unified ID 2.0 is TTD's cookieless identity solution. It uses hashed email addresses to create persistent, cross-device user IDs. 80%+ of premium publishers support UID2.

### How does TTD compare to Google DV360?
TTD is independent — it doesn't compete with publishers for ad dollars like Google does. This means TTD has better supply path transparency, no self-preferencing, and often better access to premium CTV inventory.

---

## Related Repos

- [amazon-dsp-agent](https://github.com/Synter-Media-AI/amazon-dsp-agent) — Amazon's programmatic platform
- [spotify-ads-agent](https://github.com/Synter-Media-AI/spotify-ads-agent) — Audio advertising
- [cross-platform-ads-agent](https://github.com/Synter-Media-AI/cross-platform-ads-agent) — Multi-channel management
- [audience-sync-agent](https://github.com/Synter-Media-AI/audience-sync-agent) — Sync first-party data
- [ai-creative-agent](https://github.com/Synter-Media-AI/ai-creative-agent) — Generate display & video creatives
- [conversion-tracking-agent](https://github.com/Synter-Media-AI/conversion-tracking-agent) — Attribution setup

---

## License

MIT — see [LICENSE](LICENSE) for details.

Built by [Synter](https://syntermedia.ai) · [Get API Key](https://syntermedia.ai/developer) · [Documentation](https://syntermedia.ai/docs)
