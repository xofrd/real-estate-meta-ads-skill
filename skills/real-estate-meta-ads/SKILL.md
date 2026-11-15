---
name: real-estate-meta-ads
description: Meta ads (Facebook and Instagram) for high-ticket real estate agencies and brokers in any country — intent-ladder campaign structure, higher-intent instant lead forms and click-to-WhatsApp, honest property creatives, tracking each lead from the ad to the visit and the sale in your CRM (Conversions API / Conversion Leads), scored account audit, reports an owner understands (cost per qualified lead and per visit, not CPM/CTR on their own), the Housing special ad category by country, home listings catalog, and account changes only with confirmation. Use whenever the topic is Meta Ads, Facebook Ads, Instagram Ads, Ads Manager, lead ads, lead form, real estate or property ads, new development, rentals, pixel, CAPI, audiences, creatives, "the ads bring bad leads", "how much did I spend on Meta", "audit my Meta account", ad reports, property catalog, or a request to create, pause or change something in a Meta ad account.
---

# Meta ads for real estate — working method

Most public Meta-ads skills are built for e-commerce or info-products (ROAS, urgency, bold claims). Real estate is different: **high ticket, consultative sale of roughly 90–180 days, and a lead is only worth something if it turns into a visit**. This skill rewrites good public ideas (intent ladder, day-by-day routine, change protocol) for that case. No text was copied from other projects (see the repository README, "Prior art").

## Rules that always apply

1. **Money and visits are the metric, not clicks.** CTR, CPM, likes and even cost per lead are means. The question is: *how much did each QUALIFIED lead, each VISIT and each SALE cost?* Default lead-quality funnel (adapt it and write yours down): **no-response lead ("bad lead") → pre-qualified (replied + accepted to be assisted + talks about the properties they want) → qualified (finances reviewed and still active)**. Details in `references/04-tracking-crm.md`. Bad leads are reported back to Meta as a signal, where the platform allows it.
2. **Ads amplify what already works.** A weak offer, slow follow-up or a bad page are not fixed by targeting. Diagnose the whole funnel (ad → form/WhatsApp → first reply → visit) before touching the ad.
3. **Total honesty in the creative.** Never invent scarcity ("last units", "today only"), deadlines, discounts, testimonials, numbers or "from $X" prices that do not exist. Never present an AI-generated property image as real. Checklist in `references/07-housing-and-local-rules.md`.
4. **Housing special ad category depends on where the ads run.** Required when the ads reach the US, Canada or Europe, and whenever Meta asks for it; Meta's documentation (read on 2026-11-15) says it may be set to `NONE` for advertisers outside those regions who target only audiences outside them. ⚠ Re-check before every new campaign. Meta's non-discrimination policy applies always, declared or not. The decision belongs to the advertiser; record it. Details in `references/07-housing-and-local-rules.md`.
5. **No change to the account without the owner's OK, item by item.** Everything new is created **PAUSED**. Protocol in `references/08-account-changes.md`.
6. **Data before opinion, sample before conclusion.** Always state the sample size and what it does NOT allow you to conclude. Do not rank campaigns with little volume.
7. **The CRM is the source of truth for sales**, not the Meta dashboard (Meta's attribution window is short; a property sale takes months).
8. **One business per working folder.** Keep each business's data (reports, change log) in its own folder, e.g. `meta-ads/` inside that business's project. Create folders only with the owner's approval.
9. **Reports the owner understands** (`references/06-reports.md`): answer first, in money and people, no jargon, with what to do next. Never an "agency report".

## Triage — what does the person want?

| Request | Read |
|---|---|
| Build or review campaign structure, funnel, audiences, budget | `references/01-campaign-structure.md` |
| Instant form, click-to-WhatsApp, landing page | `references/02-lead-forms-and-whatsapp.md` |
| Write or review an ad, video, image, copy | `references/03-creatives-and-copy.md` |
| Where leads that visit/buy come from, CAPI, Conversion Leads, pixel | `references/04-tracking-crm.md` |
| "Audit the account", "why are the leads bad", weekly routine | `references/05-account-audit.md` |
| Read results, build a report (weekly, monthly, per development) | `references/06-reports.md` |
| Before publishing any ad: Housing category, licensing, local ad rules, privacy | `references/07-housing-and-local-rules.md` |
| Any change in the account | `references/08-account-changes.md` |
| Property catalog (XML feed), catalog ads, catalog on WhatsApp | `references/09-property-catalog.md` |

Read only the file for the topic. A request that spans several ("build the campaign from scratch"): order 07 → 04 → 01 → 02 → 03, and stop at the end of each step for the OK.

## How the account is accessed

- **Official Meta connector (MCP, `https://mcp.facebook.com/ads`)**, added as a connector in claude.ai and authorized with OAuth (Facebook login). If its tools are available, use **read-only tools first**. The connector asks for several permissions, including `ads_management` (write): treat any write as a change under `references/08-account-changes.md`.
- **Browser mode:** read Ads Manager screens and reports through a browser-automation tool; export CSV.
- **Export mode:** the owner exports the report (CSV) and you analyze it with the criteria in `references/06-reports.md`.
- **Never a Meta access token in a file, URL or chat.** Prefer the official connector's OAuth. No third-party scripts or packages that write to the account unless the owner decides otherwise after reviewing them.

## At the end of each step

Short summary in plain language: what was done, what was **not** done, what depends on a decision and, if anything changed in the account, how to undo it.
