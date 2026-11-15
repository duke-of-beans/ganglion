# Receipt template rules: environment kickbacks

Lifted into ganglion by yokoten order wo-20261115-182038b2, from corrective action wo-20261115-5b702c13 (duke-of-beans/Gregore-private#911). Applies to every receipt and production order in this repo. Review-by: 90 days after this action verifies.

## Why

Four kickbacks in gregore were classed `environment` and each was answered "accept, nothing wrong with the work". The receipt left something implicit that the tripwire, reviewer or follow-up then read as a defect.

| Order | What happened | Rule |
|---|---|---|
| wo-20261016-379335c1 | The receipt's lock PR touched locked files, .work-orders/ and workflows, and tripped scope_out and test_lock. | R1 |
| wo-20261101-89e78b02 | Reviewer judged a truncated diff; preview checks failed on commit authorship, not on the change. | R2, R3 |
| wo-20261013-94170b2d | Deploy failures on merged PRs counted as failed attempts against an order that excluded deployment. | R4 |
| wo-20261103-54022692 | Reviewer and follow-up judged a different PR from the one that carried the work. | R5 |

## Rules

**R1. Lock PR declaration.** A receipt that locks files says in its body that its first PR is the lock PR and lists the locked paths, .work-orders/ files and workflow files it will touch. Only that PR may touch them, and it carries `lock-pr: true` in its description so the tripwire recognises it.

**R2. Reviewer sees the whole diff.** An order whose change is over 20 files or 100 KB names a verification command in `acceptance` (byte comparison or checksum). If the review diff is truncated, the reviewer runs that command instead of judging the visible part.

**R3. Name the checks that do not gate this order.** Checks unrelated to the order's paths are listed under `out_of_scope_checks`. A red check on that list is reported but neither blocks nor counts as a failed attempt. Commit author must match the repo's configured author before shipping.

**R4. Appetite counts only in-scope failures.** A failed attempt is a failure inside `scope.in`. Deploy, pairing or other excluded work is split into its own order at drafting. A deploy failure on a merged PR does not charge attempts to a save-only order.

**R5. One order, one PR trail.** The order records every PR that carries its work. Review and follow-up judge the PR named in the order's evidence. If work lands through a different repo or PR than the one under review, the evidence names the carrier PR before dispatch continues.

## Check

The action closes only when the project's environment kickback rate over the next 10 orders falls below baseline. A rule that never prevents a kickback is pruned at review-by.
