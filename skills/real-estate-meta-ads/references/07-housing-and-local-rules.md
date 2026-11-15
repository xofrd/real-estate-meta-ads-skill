# 07. Housing category and local rules — check BEFORE publishing

⚠ This file was written from research on 2026-11-15. **Meta's policies and every country's rules change: check the current version** (and, when in doubt, ask a lawyer or your licensing body) before telling a client anything.

> **Author's note:** this project is written by a broker based in **Brazil**. Examples, some details and the "optional outside the US, Canada and Europe" reading below reflect the **Brazilian market** and may be specific to it. If you operate elsewhere, check how Meta applies the rule to your country and adapt.

## 1. Housing special ad category (Meta)

### What Meta's documentation said (read on 2026-11-15)

- The Marketing API page on special ad categories (`.../audiences/special-ad-category`) says the category is **required** when the ad reaches the **United States (since 2019), Canada (since 2020) or Europe (since 2021)** — and in any other market where Meta applies the same rule.
- For an **advertiser outside those regions targeting only audiences outside them**, the field still exists (it must be filled) but may be set to **`NONE`**: declaring Housing is optional there.
- Meta's general page on real-estate ads says: "Advertisers must specify `HOUSING` as a `special_ad_category` for ad campaigns that market housing" — **without citing countries**. The two pages do not say exactly the same thing; this is why the rule must be re-checked.
- No Help Center page specific to other individual countries was found. ⚠ **re-check before publishing, and whenever Meta changes the policy.** ⚠ check which countries Meta counts as "Europe".

### When to declare Housing

| Situation | Housing |
|---|---|
| Ads reach the US, Canada or Europe (even part of the audience, e.g. investors or expats living there) | **Required** |
| Meta asks for it (in ad review, in the Ads Manager flow, or in a rejection) | **Declare**, follow the request and tell the owner |
| Advertiser outside those regions, audience only outside them | **Optional** per the documentation above (may be `NONE`). The advertiser decides; record the decision and the date |

### What declaring Housing restricts (as documented at the time of writing)

- Age fixed at 18–65+; no gender targeting.
- No lookalike audiences.
- No ZIP/postal-code or neighborhood targeting; minimum radius around a location.
- No detailed-targeting exclusions; detailed targeting limited.
- Non-discrimination certification.

Without declaring (where it is optional), lookalikes, age/gender, detailed targeting and postal code/neighborhood **remain available**. ⚠ check current list on screen.

### Always applies, declared or not

**Meta's non-discrimination policy and the law.** Never target or exclude by race, religion, national origin, sex/gender, marital status, disability or any other protected characteristic. Targeting by **location and legitimate interest related to the property** is different from excluding a protected group.

## 2. Local advertising, real-estate licensing and privacy rules — check your jurisdiction

This skill does not list country-specific laws: they differ by country, state and city, and change. Before publishing, find out what applies to you. Typical questions:

- **Licensing:** must the agency's or agent's license/registration number appear in the ad, and at what size?
- **New developments / off-plan:** is a registration, permit or approval required before marketing or taking reservations? Must its number appear in the ad?
- **Consumer protection and advertising standards:** is the advertised offer binding? What counts as misleading (price "from", size, parking, delivery date, renders, "last units")? Is there an advertising self-regulation code?
- **Privacy laws** (for example GDPR, LGPD, CCPA): lawful basis and purpose for forms, customer-list audiences and CAPI; privacy policy; cookie consent before the pixel; data subject rights.
- **Fair housing / anti-discrimination** rules for housing ads, in addition to Meta's policy.

When unsure, ask a lawyer or your licensing body. Do not state a rule to a client that you have not checked.

## 3. Privacy (general minimum)

- Purpose and **privacy policy** on the form.
- **Lawful basis** to upload CRM customer lists as audiences and to send data via CAPI.
- Cookie consent before the pixel, where required.
- Phone/email sent to Meta **hashed**. No personal data in reports.

## 4. Quick checklist per ad

- [ ] License/registration numbers shown where required
- [ ] New development: registration/permit required by your jurisdiction obtained and shown if required
- [ ] Price/size/delivery date/parking = contract/official specification
- [ ] Illustration labeled; no AI image passed off as real
- [ ] No invented scarcity/urgency/testimonials; no guaranteed returns
- [ ] Audience does not discriminate against any protected group
- [ ] Countries reached checked: US, Canada or Europe? → declare Housing
- [ ] Form with privacy policy; pixel with consent where required
- [ ] Property still available today
