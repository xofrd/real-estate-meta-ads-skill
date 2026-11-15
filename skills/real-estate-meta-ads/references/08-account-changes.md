# 08. Changes to the account — Confirm → Execute → Verify protocol

Applies to EVERY change: create, activate, pause, budget, audience, ad, form, automated rules, applying a Meta recommendation. No exceptions, even if someone says "you can do everything".

## 1. Confirm (before)

```
## Proposed change
Account: <name> (<ID, without exposing personal data>)
Where: campaign / ad set / ad
What it is: <plain language>
Before: <state read NOW on screen or via the API, not from memory>
After: <new state>
Effect on spend: <e.g. $50/day → $60/day ≈ +$300/month>
Risk: low / medium / high
How to undo: <exact step>
```

- Show **the impact before asking for the OK**.
- Batches: ≤ ~50 items per confirmation, listed one by one. Pausing and deleting are separate confirmations. **Delete only when explicitly asked** — prefer pausing. (Also applies to any tool with `delete`.)
- Budget increases: **at most 2× at a time** and never above the agreed ceiling. A generic authorization ("you can adjust the budget") **does not count**: budget is always per campaign.

## 2. Execute

- Everything created starts **PAUSED**. **Creating and activating are never the same step**: activating is a new confirmation.
- Do not touch an ad set in its **first 3 days** (learning) and do not swing the budget.
- Before optimizing, **read the last 3 days of `change-log.md`** (do not undo what was just done).
- Log in the business's `meta-ads/change-log.md`: date/time, what, before, after, reason, how to undo.
- **Browser mode:** one change at a time; read the screen before and after; do not trigger browser confirmation dialogs without warning.
- **Official Meta connector:** start with read-only tools. For writes, create paused and then check the real status and ad approval. If the account offers protective rules (block activation, cap budget), suggest turning them on.
- If pixel/CAPI is broken: **stop** and fix it before creating campaigns.

## 3. Verify (after)

- Re-read the screen/API: is the state really the proposed one? Ads approved? Status PAUSED/ACTIVE as agreed?
- Tell the owner what was done, what was not, and how to undo it.

## Access security

- **Never a Meta access token in a `.env` file, a URL, or pasted into the chat.** Prefer the official connector's OAuth login.
- **Start read-only.** A news report (Digiday) mentioned ad accounts restricted after using Claude Code with the Meta connector, with no confirmed cause. ⚠ not verified by this project.
- Do not install third-party packages/scripts that write to the account without reviewing them (who holds the token, what they can do, whether there is a dry-run/spend cap/log).
- Policy warning or restricted account: stop and tell the owner; do not insist.
