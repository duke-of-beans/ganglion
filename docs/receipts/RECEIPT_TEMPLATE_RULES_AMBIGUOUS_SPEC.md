# Receipt template rules: ambiguous_spec kickbacks

Lifted into ganglion by yokoten order wo-20261121-40133c93, from corrective action wo-20261120-752df3f2 (duke-of-beans/Gregore-private#1104). Applies to every receipt and production order in this repo. Review-by: 90 days after this action verifies.

## Why

Three kickbacks in gregore were classed `ambiguous_spec`. In every one the work was accepted — the change stood, nothing was wrong with it — but the receipt left the intent boundary open enough that the reviewer could not tell in-scope from out-of-scope, and in one case the ambiguity had to be resolved by David himself.

| Order | What happened | Rule |
|---|---|---|
| wo-20261016-379335c1 | The lock PR touched locked files, .work-orders/ and workflows by design — it was the lock's own order. The reviewer flagged it because the receipt did not say the lock PR is the in-scope exception to the lock. | A1 |
| wo-20261106-ee821b16 | The worker added a true but unrequested line. The reviewer flagged it because the receipt did not say whether unrequested true facts may appear. | A2 |
| wo-20261119-a15454de | The ambiguity was not resolvable from the receipt and went up to David from the asks screen. | A3 |

## Rules

**A1. Name the in-scope exception to the rule.** A receipt that states a constraint ("never touch locked files") also names every exception ("except this order's own lock PR") in the same sentence. An exception the reviewer has to infer is a miss, even when the inference is correct.

**A2. State whether unrequested true facts may appear.** A receipt that names a deliverable also states whether the worker may add true but unrequested content (an extra line, an extra field, a clarifying note) to that deliverable. If it may, say so and bound it ("true facts only, no scope expansion"). If it may not, say so. Silence reads as permission, and permission the receipt never granted is a miss.

**A3. The receipt must be resolvable without the author.** If a reviewer or the follow-up has to ask the author (or David) what the receipt meant, that is a miss even when the answer is obvious in hindsight. The body must carry enough intent that a fresh reader reaches the same boundary decision.

## Applying it

Before a receipt or production order goes out, answer three questions in the body:

1. **Exception.** Does the receipt state a constraint with an exception? Name the exception in the same sentence as the constraint, or state that there is none.
2. **Unrequested content.** May the worker add true but unrequested content to the deliverable? Say yes (and bound it) or no. Silence reads as permission.
3. **Resolvability.** Would a fresh reader, given only the receipt, reach the same boundary decision the author did? If not, add the missing intent.

## Check

The action closes only when the project's ambiguous_spec kickback rate over the next 10 orders falls below baseline. A rule that never prevents a kickback is pruned at review-by.

## Related

`docs/receipts/RECEIPT_TEMPLATE_RULES.md` covers `environment` (R1–R5) in this repo. This document covers `ambiguous_spec` (A1–A3). The two are complementary: R governs what the receipt *declares*, A governs how it *reads*.
