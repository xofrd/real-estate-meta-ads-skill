# 05. Account audit — scored checklist for real-estate leads

Format inspired by public scored audits, rewritten for high-ticket leads. Each item: **OK / Warning / Fail / Quick win**. Score per block 0–100 and a weighted overall score. **Read the account before giving an opinion; never audit from memory.**

## Block A — Tracking and signal (weight 30%)
- [ ] Pixel firing on the right events; deduplication by `event_id` (browser × server)
- [ ] CAPI active; EMQ ≥ 8 on lead events
- [ ] Domain verified; event priority checked (Lead above purchase)
- [ ] CRM stages (qualified/visit/sale) reaching Meta ≥ 1×/day
- [ ] `lead_id` and UTMs stored in the CRM; % of leads without source
- [ ] Consent banner before the pixel, where required
- [ ] Data lag explained in reports

## Block B — Funnel and lead quality (weight 30%)
- [ ] "Qualified" defined in writing
- [ ] Higher-intent form with 3–5 qualifying questions
- [ ] Time to first reply and an owner per shift
- [ ] Lead → qualified → visit rate per campaign (not only cost per lead)
- [ ] CTWA: cost per conversation, reply rate, cost per reply
- [ ] Retargeting reported separately from prospecting

## Block C — Structure (weight 20%)
- [ ] % of ad sets in *Learning Limited* (target ≤ 30%)
- [ ] Daily budget ≥ ~5× the target cost per optimized event
- [ ] Audiences exclusive between rungs; customers and sold properties excluded
- [ ] Audience Network/placements checked
- [ ] Standard names; UTMs on every ad
- [ ] Sold/unavailable property with its ad paused
- [ ] Housing special ad category decision recorded and correct for the countries reached

## Block D — Creative and compliance (weight 20%)
- [ ] 3+ active concepts; fatigue/frequency under control
- [ ] Ads without fake scarcity/urgency, no generated image passed off as real
- [ ] License/registration numbers shown where your jurisdiction requires; price/size checked
- [ ] Privacy policy on the form

## Audit output

1. **Overall and per-block score**, in a 4-row table.
2. **The 3 biggest money leaks** (estimated in money per month, stating the uncertainty).
3. **Quick wins** (≤ 1 hour each, low risk).
4. **What could not be verified** and why.
5. A plan in order of impact; every change goes through `08-account-changes.md`.

## Routine

- **Weekly (15 min):** spend, leads, qualified, visits, reply time; anomalies; no changes in the first 3 days of a new ad set.
- **Monthly:** full report (`06-reports.md`), quick audit of blocks A and B.
- **Quarterly:** revisit the definition of qualified, the funnel and the budget per property type.
