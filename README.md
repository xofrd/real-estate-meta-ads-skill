# real-estate-meta-ads-skill

**English** · [Português (Brasil)](README.pt-BR.md)

A Claude skill for running Meta ads (Facebook and Instagram) for **high-ticket real estate**: agencies, brokers and developers selling or renting property, in any country.

It is a working method, not software. It tells Claude how to structure campaigns, write honest property ads, track a lead from the ad to the visit and the sale in your CRM, audit an account, write reports an owner can read, handle Meta's Housing special ad category, use a property catalog, and change anything in the account only after explicit confirmation.

No promises of results. Ads amplify what already works; they do not fix a weak offer or slow follow-up.

## Who it is for

- Real-estate agencies, brokers and in-house marketing teams that buy Meta ads themselves.
- Agencies or freelancers serving real-estate clients who want a stricter, honest method.
- Anyone whose sale is long (months), high-value, and depends on a visit — the method may fit other consultative sales too, but it was written for property.

It is **not** built for e-commerce, ROAS optimization or high-volume cheap leads.

## What is inside

```
skills/
  real-estate-meta-ads/          English
    SKILL.md
    references/01..09-*.md
  real-estate-meta-ads-pt-br/    Brazilian Portuguese (same content)
    SKILL.md
    referencias/01..09-*.md
```

| # | Topic |
|---|---|
| 01 | Campaign structure: intent ladder, budget split, funnels per property type, naming, routine |
| 02 | Higher-intent instant forms, click-to-WhatsApp, landing pages, speed to lead |
| 03 | Honest creatives and copy; forbidden claims |
| 04 | Tracking to your CRM: lead stages (no-response → pre-qualified → qualified), Conversion Leads, CAPI |
| 05 | Scored account audit (4 blocks) |
| 06 | Reports in money and people, not CPM/CTR |
| 07 | Housing special ad category by country; local advertising, licensing and privacy rules (generic) |
| 08 | Change protocol: Confirm → Execute → Verify; everything created paused; access security |
| 09 | Property catalog (`home_listings` feed) for Facebook/Instagram; what WhatsApp does and does not support |

## Install

Install **one** language version (both have the same triggers and would compete).

```bash
git clone <repository-url>
cp -r real-estate-meta-ads-skill/skills/real-estate-meta-ads ~/.claude/skills/
# or, for Brazilian Portuguese:
cp -r real-estate-meta-ads-skill/skills/real-estate-meta-ads-pt-br ~/.claude/skills/
```

For a single project, copy the folder to `.claude/skills/` inside that project instead. Other Claude apps that support skills may accept the folder as a ZIP upload; check your app's documentation.

Claude loads the skill when the conversation is about Meta/Facebook/Instagram ads, lead forms, property ads, pixel/CAPI, audits or ad reports.

### Connecting to your Meta ad account (optional)

The skill works without any connection (paste or export CSV reports). To let Claude read the account:

1. In **claude.ai** (browser): Settings → Connectors → add a custom connector with the URL `https://mcp.facebook.com/ads` and authorize with Facebook (an account with access to the ad account).
2. Reopen Claude Code: the tools should appear under the connector's name.
3. Access may be enabled account by account; you may see `is_ads_mcp_enabled: false`.

Notes from our own setup (⚠ may have changed): OAuth started from the Claude Code terminal failed with `redirect_uris are not registered`, while adding the connector through claude.ai was the path expected to work. The connector requests several permissions, including `ads_management` (write). A news report (Digiday) mentioned ad accounts restricted after using Claude Code with the connector, with no confirmed cause. **Start read-only.**

Never put a Meta access token in a file, a URL or the chat. See [SECURITY.md](SECURITY.md).

## Examples

- "Audit my Meta ad account for lead quality." → scored audit, top 3 money leaks, what could not be verified.
- "Here is last month's CSV export. Write the report for the owner." → one-page report: what happened, what it means, one recommendation, funnel in money.
- "Write three ads for a resale 2-bedroom apartment near the station." → specific, honest copy with a test grid, plus the pre-publish checklist.
- "We want to reach investors living in Portugal. Do we need the Housing category?" → yes (Europe), and what that restricts.
- "Pause the ad for the sold unit." → a confirmation block (before, after, spend effect, how to undo) and nothing done until you say yes.
- "Can our property XML feed become a catalog for Instagram and WhatsApp?" → required fields, what is confirmed, what is inference, a paused test plan.

## Status and limitations

- **Written from Brazil.** The author is a real-estate broker in Brazil. Some details are specific or characteristic of the Brazilian market (for example, how the Housing special ad category applies when you advertise only inside Brazil, WhatsApp-centered sales, currency and number formats such as `205,65`). If you operate elsewhere, treat those parts as examples and check your local rules.

- **Version 0.1.0.** Written from the day-to-day work of a real-estate brokerage. **Not yet tested at scale** or across many countries and account types.
- **Meta changes its policies, products and requirements often.** Everything dated 2026-11-15 and every `⚠ check` mark must be re-verified against Meta's current documentation before you rely on it.
- **Not legal advice.** The skill deliberately does not list country-specific laws. Check advertising, real-estate licensing, consumer-protection and privacy rules where you operate (privacy laws such as GDPR, LGPD or CCPA are mentioned only as examples).
- Open questions not verified: whether Conversion Leads accepts a negative "bad lead" event for training; whether Ads Manager forces the Housing category on home-listings catalog campaigns outside the required regions; whether unofficial WhatsApp integrations can send conversation conversions back to Meta.
- Not affiliated with, endorsed by or sponsored by Meta or Anthropic. Product names belong to their owners.

## Prior art and method

On 2026-11-15 we read 14 public Meta-ads skills and MCP servers to see what already existed. Most were built for e-commerce or info-products; none covered long-cycle qualified leads, Conversion Leads with CRM stages, or real-estate rules. We did not publish scores: they reflected one use case and one reviewer, not the general quality of those projects. Names are as recorded at the time; links and status were not re-verified for this release.

**Nothing was copied.** Where we took an idea, it was rewritten in our own words for real estate. `hoodini/meta-ads` had no license file at review time, so only ideas were used, never text.

| Project (as named at review) | What we took |
|---|---|
| Official Meta MCP (`mcp.facebook.com/ads`) | Recommended connection; read-only first |
| hoodini/meta-ads | Ideas rewritten: intent ladder, day-by-day routine, click-to-WhatsApp, account-write protocol |
| Adspirer Lead Gen Machine | Idea of ranking by qualified lead, not by lead |
| thatrebeccarae/facebook-ads | Scored-audit format |
| attainmentlabs (MCP) | Safety ideas: dry-run, spend cap, change log |
| dengineproblem | Idea of keeping an action history (repository no longer available at review time) |
| Pipeboard | Not used (third-party access to the token) |
| openclaudia, arnabbagxd, dvorkinguy, kostja94, Rioja, Varnan-Tech, claude-office-skills | Reviewed; nothing used here |

## Contributing

Corrections are especially welcome when Meta changes a policy. Read [CONTRIBUTING.md](CONTRIBUTING.md): cite official sources, no hype, no private data. Conduct: [CODE_OF_CONDUCT.md](CODE_OF_CONDUCT.md). Changes: [CHANGELOG.md](CHANGELOG.md).

## License

[MIT](LICENSE).
