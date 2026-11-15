# 02. Instant forms, WhatsApp and landing pages

Goal: a lead the agent can turn into a visit. Raw lead volume is vanity.

## Instant form — "Higher intent" type

- Use the **Higher intent** type (review screen before submitting). Expect less volume and more quality (third-party estimates: 20–40% fewer leads; not confirmed by Meta).
- 3 to 5 questions, in order of effort:
  1. To **live in or to invest**?
  2. **Price range** of the property (ranges, not an open field).
  3. **Timeframe** to decide.
  4. **Payment** (mortgage pre-approved / cash / still running the numbers / other options available in your market).
  5. **Preferred channel** (WhatsApp or call) and best time.
- Name, email and phone prefilled; phone with country and area code.
- **Privacy policy** with a real link and a purpose statement (required by most privacy laws).
- Thank-you screen saying **what happens next and when** ("an agent will message you on WhatsApp within X minutes") — and keep the promise.
- The form `lead_id` (15–17 digits) **must be stored in your CRM**: it is the key to send stages back to Meta.
- ⚠ check: at the time of writing the official Meta connector did not create instant forms; build the form **by hand in Ads Manager** unless the current tool list says otherwise.
- Respect office hours: a form that arrives at 11 pm and is answered at 9 am loses the lead. Consider an honest auto-reply ("we got it, we will reply at 9 am").

## Click-to-WhatsApp (CTWA)

- Requires a WhatsApp Business account linked to the Page and a verified number **before spending**.
- Prefilled message that identifies the ad/property ("Hi, I saw the Green Park apartment").
- Own metrics: **cost per conversation started → reply rate (lead's first reply) → cost per reply → cost per visit**. If people start conversations and do not reply or buy, the bottleneck is **follow-up**, not the ad.
- ⚠ Sending conversions from conversations back to Meta (Conversions API for messaging) requires the **official** WhatsApp Business Platform and the `ctwa_clid` identifier. **Not verified:** whether unofficial WhatsApp integrations used by some CRMs can close that attribution. Until verified, measure with what your CRM records (source + stage) and do not promise optimization on WhatsApp conversions.

## Speed and lead ownership

- Set a **maximum time to first contact** and **one named owner** per shift. Cheap leads nobody answers is the most common (and most expensive) mistake.
- Measure time to first human/AI reply in the CRM and cross it with the visit rate.

## Landing page (when there is one)

- The ad's promise appears **identically** on the page; call to action above the fold.
- Real data: size, layout, delivery date, conditions, a price or range **that exists**; illustrative images labeled as such.
- License/registration numbers where your jurisdiction requires them (see `07-housing-and-local-rules.md`).
- Cookie/consent banner **before** the pixel fires, where privacy law requires it.
- Events: `PageView`, `ViewContent`, an engaged-visit custom event (30 s or 60% scroll), WhatsApp click, form submission — with **deduplication by `event_id`** between browser and server.
