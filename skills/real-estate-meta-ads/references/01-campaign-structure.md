# 01. Campaign structure and the intent ladder

Idea adapted (rewritten) from the "intent ladder" method found in public skills, translated to property. Each rung has **its own audience, its own message, and excludes the rungs above it**.

## Rungs

| Rung | Who | Message | Goal |
|---|---|---|---|
| 0 Cold | Never saw us | Show the property/area with facts (floor plan, size, location, real condition) | Bring them to the page/form |
| 1 Watched the video (≥ 50%) | Got interested | Go deeper: real differentiators, video of the site | Lead them to the development/property page |
| 2 Visited the page | Browsed | Proof (construction progress, delivery, references) and a concrete invitation | Form or WhatsApp |
| 3 Really engaged | ≥ 30 s on the page or 60% scroll (custom event, e.g. `EngagedVisit`) | Direct invitation to talk/visit | Lead |
| 4 Clicked WhatsApp / opened the form and did not finish | Almost a lead | Make it easy: "ask your question in 2 minutes" | Lead |
| 5 Lead | In your CRM | **Leaves prospecting ads** | Human/AI follow-up |
| 6 Qualified → Visit → Offer → Sale | CRM funnel | Out of all prospecting (a closed sale never sees an ad for the same property) | Measure and send back to Meta |

Mutually exclusive audiences: whoever moves up leaves the previous rung. Buyers leave everything.

## Budget split (starting point, not dogma)

- Prospecting (0–1): ~65–75% · Re-engagement (2–4): ~15–25% · Closing (visit/offer pending): ~5–10%.
- Budget too small for three layers? Start with **prospecting + retargeting of page visitors** only. Do not slice the budget below what gives minimum volume for learning.
- Retargeting looks cheap because it reaches people who were going to buy anyway. **Report prospecting and retargeting separately** and do not credit retargeting with the sale it only harvested.

## Different funnels (do not mix)

| Type | Particularity |
|---|---|
| New development / off-plan | May require registration or a permit before marketing in your jurisdiction (see `07-housing-and-local-rules.md`); long cycle; builds an interest list |
| Resale / ready to move | Shorter cycle; specific property; stock changes — pause the ad of a sold property the same day |
| Rentals | Lower ticket, high volume; qualification by income/guarantor; its own metrics |
| Owner acquisition (listings) | Different audience and message (people who want to sell/rent theirs) |

## Naming convention

`<BRAND> | <type> | <development/area> | <objective> | <rung> | YYYY-MM`
Example: `ACME | NewDev | Green Park | Lead-Form | R0 | 2026-11`. Same logic for ad sets and ads (`<angle>_<format>_v<n>`).

## Campaign objective

- **Leads** (instant form, "higher intent" type) or **Messages/WhatsApp**. Do not use Traffic or Engagement "because conversions are low": that brings people who click and like, not people who buy.
- Optimize for the **deepest event that still has volume** (see `04-tracking-crm.md`): usually *pre-qualified* at first, then *qualified* or *visit scheduled* when volume allows; rarely *sale* (Meta asks for roughly 200 leads/month and the target event within 28 days; a property sale almost never fits). ⚠ check current requirements.
- Placements: start with Automatic but **check Audience Network** (it often spends budget on poor leads); turn it off if the report shows that.
- Watch Advantage+ stretching age/location beyond what the property serves. Check the audience actually reached.

## Audiences

- Radius/neighborhoods of the property and the areas where its buyers actually come from; lookalike of **customers who visited/bought** (not of "all leads").
- Lookalikes, age/gender and detailed targeting are **not available** when the Housing category is declared (see `07-housing-and-local-rules.md`). Plan the structure after deciding the category.
- Avoid the "ideal" 1–10 million audience: for a regional agency it is far too large.
- Uploading a CRM customer list as an audience requires a lawful basis under the privacy laws that apply to you (see `07-housing-and-local-rules.md`).
- Declared or not, **never target or exclude by discriminatory criteria** (Meta's policy always applies).
- ⚠ check: detailed-targeting exclusions were reported as removed by Meta in January 2026 — confirm the current state on screen.

## Routine (anti-over-tweaking)

- **Day 0:** structure, tracking tested, everything paused until the OK.
- **Days 1–3:** do not touch (learning phase). Only check delivery and errors.
- **Day 4+:** decide using the table below, with a minimum sample.
- Log every change in a `change-log.md` (date, what, before, after, why).

| Situation (with enough sample) | Action |
|---|---|
| Cost per qualified lead/visit good and stable | Keep; scale budget in small steps (≤ 20% at a time) |
| Cheap leads, nobody answers/qualifies | **Not the ad**: audit follow-up and the form |
| Creative expensive and no qualified lead after the minimum | Pause the creative, not the campaign |
| Low delivery | Review audience, budget and rejections before blaming the creative |
| Not enough data | Say "we cannot conclude yet" and how much is missing |

Test order: **hook → angle → format → offer → audience**, one at a time; a 3×2×2 grid (3 concepts × 2 hooks × 2 copies) when the budget allows.
