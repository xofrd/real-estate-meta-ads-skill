# 06. Reading results and writing reports that make sense

Goal: a **meaningful** report, not an unreadable "agency report". Rule: the reader should not need to know what CPM means.

## Principles

1. **Answer first.** The first 3 lines say: *what happened, what it means, what to do.*
2. **Everything in money and people.** "We spent $4,200 and it produced 38 contacts, 11 qualified and 4 visits; each visit cost $1,050." Not "CPM $38, CTR 1.2%". Use the business's own currency.
3. **Funnel metrics, in order:** spend → leads → **qualified** → **visits** → offers → sales; cost of each rung; % passing between rungs.
4. **Compare with something:** previous period, same campaign, agreed target. A number without comparison says nothing.
5. **Say what we do NOT know:** small sample, delayed data, leads without source, Meta × CRM divergence. Never hide it.
6. **One main recommendation** (and at most two secondary ones), with reason, cost and risk. No list of 15 "opportunities".
7. **Cause before blame:** if leads are cheap and do not become visits, investigate follow-up/qualification before blaming the creative.
8. **No vanity:** likes, reach, CPM, CTR appear only to support a specific diagnosis (e.g. "the creative is tired: frequency 5.1").
9. **No personal data** (name, phone) in the report.

## Template (one-page summary + detail)

```
# Meta Ads — <period> — <business/development>

## In 3 lines
1. What happened: ...
2. What it means: ...
3. What I recommend: ... (your decision: yes/no)

## The funnel in money
| Stage | Qty | Cost per unit | vs. previous period |
|---|---|---|---|
| Spend | $ | | |
| Leads | | $ | |
| Qualified | | $ | |
| Visits scheduled / done | | $ | |
| Offers / Sales | | $ | |
(Source: spend = Meta; the rest = CRM. Leads without source: N = X%.)

## What worked and what did not
- Best ad/campaign by **cost per visit** (not cost per lead), with sample.
- Worst, and what to do (pause / test another angle / fix follow-up).

## Follow-up (the hidden bottleneck)
Average time to first reply; % of leads answered within X min; lead → visit rate by reply-time band.

## Before concluding
Sample, data lag, divergences, what we still cannot claim.

## Decisions requested
1) ... 2) ...  (each one goes through the change protocol)
```

## How to read the numbers (cheatsheet)

| Symptom | Likely cause | Check first |
|---|---|---|
| Low cost per lead, almost no qualified | Form too easy / audience too broad / Audience Network | Qualifying questions; report by placement |
| Many WhatsApp conversations, few replies | Slow follow-up or mismatched message | Time to first reply; prefilled text |
| Cost per lead jumped | Creative fatigue / seasonality / auction competition | Frequency; creative; date of the change |
| Good visits, zero sales (cycle too short to tell) | Too early | 90–180-day window; say "inconclusive" |
| Meta dashboard ≠ CRM | Attribution window / leads without source / duplicates | Count no-source leads; deduplicate |
| Retargeting "with great ROAS" | Harvested people who were going to buy anyway | Separate from prospecting; holdout test |

## Minimum sample (rule of thumb, adjust)

- Do not compare ads with fewer than ~30 leads each or fewer than 7 days of delivery.
- Do not decide on "sales" in a campaign with few sales: use qualified/visit and state the uncertainty range.
- A weak conclusion becomes a "hypothesis to test", not a "fact".

## Delivery formats

- **Chat/terminal:** short summary in plain language (always).
- **Full report:** 1–2 page HTML/PDF for the owner/partners, on request. A chart only when it shows a real trend or comparison; the funnel as horizontal bars in money.
- **File:** `meta-ads/reports/YYYY-MM-DD-<period>.md` inside the business's own folder (create the folder only with approval).
- Language: the owner's language, short sentences, explain each acronym the first time.
