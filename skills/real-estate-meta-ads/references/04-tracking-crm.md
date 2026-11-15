# 04. Tracking: from the ad to the sale, through your CRM

The core problem (no public skill reviewed solved it): a property sale takes 90–180 days and Meta's attribution window is about 7 days. The approach is to **send funnel stages back to Meta** (Conversion Leads) and **measure the truth in your CRM**.

## 1. Define "qualified" (mandatory before analyzing)

Default definition in three rungs — adapt it to your business and write it down:

| Stage | Rule | What it becomes for Meta |
|---|---|---|
| **No-response lead** ("bad lead") | Came in and **never replied** to the first contact (deadline to agree, e.g. 7 days) | Negative signal: Meta learns what is NOT good (⚠ see below) |
| **Pre-qualified lead** | **Replied** + **accepted to be assisted** (curated search / follow-up) + talks about the properties they are looking for | Positive volume event (good for optimization) |
| **Qualified lead** | After reviewing what they want and their **finances** (income, down payment, financing, etc.) **and still active**; likely to book a visit | Positive higher-value event |

Edge rules to decide: how long a no-response lead waits before becoming a bad lead; what "still active" means (e.g. replied in the last X days); whether the definition differs for new developments, resale and rentals.

Without this definition applied to the data, analysis stops: **"blocked: leads have no stage in the CRM"**.

## 2. Stages and events

`lead` → (`no response` | `pre-qualified`) → `qualified` → `visit scheduled` → `visit done` → `offer` → `sale`.

- **Sending the bad lead back to Meta:** send the no-response stage through the same channel (CAPI / CRM integration). ⚠ **Not verified:** whether the Conversion Leads documentation accepts a negative / "lost lead" event for training. If not, the signal is indirect: Meta learns from the contrast between who moved forward and who stayed put, so **every positive stage must arrive with the `lead_id`**. Do not promise the effect before testing.
- Optimize first for **pre-qualified** (replies + accepts assistance): it is fast and has volume, which fits Meta's requirements. Move to **qualified** or **visit scheduled** when they have volume; do not optimize for **sale** (Meta asks for roughly 200 leads/month, the target stage within 28 days and a conversion rate between about 1% and 40%; a property sale usually takes longer than 28 days and stays below 1%). **Send the sale anyway**, to measure. ⚠ check current requirements.
- Send **at least 2, preferably 3+** stages to Meta (CRM integration / Conversion Leads via CAPI), at least **once a day**, always to the **same pixel/dataset**.
- Store in the CRM, per lead: `lead_id` (form), UTMs (campaign/ad set/ad), `ctwa_clid` / WhatsApp click source (if available), date of each stage.
- ⚠ check: training reportedly takes 1–2 months and works only with instant forms. Verify these requirements in the current documentation before promising anything (policy changes).

## 3. Signal quality (CAPI)

- **Deduplication by `event_id`** between pixel and server.
- Target **Event Match Quality (EMQ) ≥ 8**. Parameters: email and phone **hashed**, `fbc`, `fbp`, `external_id`.
- Domain verified and event priority checked. For a real-estate agency, **Lead (and its stages) weighs more than Purchase** — the opposite of what e-commerce skills teach.
- Data lag: CRM events arrive later; warn in reports that the last days are incomplete.

## 4. Source without loss

- Every lead has a source: campaign/ad/form/WhatsApp/organic. **Count leads without a source separately** (how many, % of total) and never hide them.
- Duplicate leads: deduplicate by normalized phone number before counting. Record rejected ones.
- Always cross: **spend (Meta) × leads (CRM) × visits × sales (CRM)**. When Meta's dashboard and the CRM disagree, the CRM wins, with the difference explained.

## 5. Privacy in tracking

- A lawful basis and stated purpose for using data in audiences/CAPI under the privacy laws that apply to you (e.g. GDPR, LGPD, CCPA); privacy policy reachable from the form.
- Cookie consent before the pixel, where required.
- **Do not enrich leads by scraping search engines or AI tools** (privacy risk).
- Personal data (phone, email) never in reports, logs or URLs.

## 6. Known open questions

- Unofficial WhatsApp integrations may **not** allow conversation conversions via CAPI: not verified.
- Map where your CRM stores `lead_id` and UTMs before promising stage upload.
