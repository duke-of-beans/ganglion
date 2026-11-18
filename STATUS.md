# GANGLION — STATUS

Status: infra
Last Updated: 2026-11-18
Last Recorded: wo-20261117-ffa284d3 — Install fleet-preview on Sentinel and prove one gated link end to end

<!-- work-orders:begin (generated from portfolio.orders by the record step; edits inside this block are overwritten) -->
## Work orders

_Generated 2026-11-18T06:31:02.814Z from the work-order store. Done means verified and recorded; the live view is GregLite._

**Project:** ganglion (GANGLION, infra)

### Waiting on David

Nothing.

### In flight

| Order | Project | State | Title | Updated |
|---|---|---|---|---|
| `wo-20261117-5ed6543d` | ganglion | dispatched | Effector CLIs start with an empty env; read-back output is scrubbed of key shapes | 2026-11-18 |
| `wo-20261117-0768dfb0` | ganglion | drafted | Replay evals P2: first set (Gregore-private, 20 tasks) and baseline of OpenCode + Claude lanes | 2026-11-17 |
| `wo-20261117-ce327c83` | ganglion | drafted | Sentinel router checkout follows main (git-plane reconcile) | 2026-11-17 |
| `wo-20261106-a8af50fa` | ganglion | drafted | Trim OpenCode prompt weight per GANGLION dispatch | 2026-11-06 |

### Receipts

None.

### Open kickbacks

None.

### Recently recorded (last 30 days)

- 2026-11-18 `wo-20261117-0741f7d4` **Preview links: an agent builds an app on Sentinel, David gets a gated link (orgo-deploy pattern)** (ganglion) — [duke-of-beans/ganglion-private#87](https://github.com/duke-of-beans/ganglion-private/pull/87) · merged, checks green, deployed
- 2026-11-18 `wo-20261117-542aaf69` **G7 WSL lane: take full repo jobs (Claude lane, more slots, per-worktree locks)** (ganglion) — every child order is verified, recorded, cancelled or superseded
- 2026-11-18 `wo-20261117-876b99fb` **Native G7 effector: successful runs end with "The system cannot find the path specified" and exit 1** (ganglion) — [duke-of-beans/ganglion-private#90](https://github.com/duke-of-beans/ganglion-private/pull/90) · merged, checks green, deployed
- 2026-11-18 `wo-20261117-ffa284d3` **Install fleet-preview on Sentinel and prove one gated link end to end** (ganglion) — [duke-of-beans/ganglion-private#91](https://github.com/duke-of-beans/ganglion-private/pull/91) · merged, checks green, deployed
- 2026-11-18 `wo-20261117-eec95b81` **greg-backend: fix the red lane-context test and the leftover "Home" names** (ganglion) — [duke-of-beans/greg-backend#59](https://github.com/duke-of-beans/greg-backend/pull/59) · merged, checks green, deployed
- 2026-11-18 `wo-20261117-c5b5e72a` **Lane rules: one writer per checkout, self-reports aren't evidence, usage-limit means unavailable until reset** (ganglion) — [duke-of-beans/ganglion-private#89](https://github.com/duke-of-beans/ganglion-private/pull/89) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-a5a5a4ad` **Replay evals P1: miner, runner, keep rule (src/replay/)** (ganglion) — [duke-of-beans/ganglion-private#83](https://github.com/duke-of-beans/ganglion-private/pull/83) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-c85d4a83` **Replay evals: evals.replay-freeze action class (mine + verify + commit set, no model)** (ganglion) — [duke-of-beans/ganglion-private#85](https://github.com/duke-of-beans/ganglion-private/pull/85) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-59d77b1f` **Action classes ignore harness-owned params (max_usd, max_steps, order_id) that the money-guard trigger adds** (ganglion) — [duke-of-beans/ganglion-private#86](https://github.com/duke-of-beans/ganglion-private/pull/86) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-9c58bd1c` **Replay evals P3a: evals.replay action class (no model), detached runner, verdict receipt to Greg** (ganglion) — [duke-of-beans/ganglion-private#84](https://github.com/duke-of-beans/ganglion-private/pull/84) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-c519c2a6` **ops-context ganglion.md: current router paths, G7 lanes, slots, repo-lock slots** (ganglion) — [duke-of-beans/ops-context#176](https://github.com/duke-of-beans/ops-context/pull/176) · merged, checks green
- 2026-11-17 `wo-20261117-91a2e289` **Bake-off Qwen4-Max vs Kimi for the OpenCode lane, swap if it wins** (ganglion) — [duke-of-beans/ganglion-private#81](https://github.com/duke-of-beans/ganglion-private/pull/81) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-5cf5d07b` **Router: pending reaper must not hold rows waiting on a busy capable effector** (ganglion) — [duke-of-beans/home#57](https://github.com/duke-of-beans/home/pull/57) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-64f09cd8` **Router: up to N concurrent jobs per repo (each has its own worktree and branch)** (ganglion) — [duke-of-beans/greg-backend#58](https://github.com/duke-of-beans/greg-backend/pull/58) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-fff1fd95` **Effector: per-repo clone/fetch mutex for parallel jobs; OpenCode prompt contract** (ganglion) — [duke-of-beans/ganglion-private#82](https://github.com/duke-of-beans/ganglion-private/pull/82) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-e8899da2` **Loop-safe admission and one-output-per-cause for chained dispatches (from slack-agent-mesh)** (ganglion) — [duke-of-beans/ganglion-private#77](https://github.com/duke-of-beans/ganglion-private/pull/77) · merged, checks green, deployed
- 2026-11-17 `wo-20261117-b22f7044` **Effector: scratch off tmpfs, per-dispatch TMPDIR, write gate, empty output fails** (ganglion) — [duke-of-beans/ganglion-private#76](https://github.com/duke-of-beans/ganglion-private/pull/76) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-182038b2` **Yokoten: environment fix from gregore** (ganglion) — [duke-of-beans/ganglion#24](https://github.com/duke-of-beans/ganglion/pull/24) · merged, checks green
- 2026-11-15 `wo-20261115-6a635cd0` **MAX usage sign-in without a terminal (Sentinel reader)** (ganglion) — [duke-of-beans/ganglion-private#74](https://github.com/duke-of-beans/ganglion-private/pull/74), [duke-of-beans/Gregore-private#904](https://github.com/duke-of-beans/Gregore-private/pull/904) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-0fdda381` **MAX plan usage reader on Sentinel** (ganglion) — [duke-of-beans/ganglion-private#73](https://github.com/duke-of-beans/ganglion-private/pull/73) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-f160b884` **OpenCode lane: allow harmless shell glue so runs aren't killed** (ganglion) — [duke-of-beans/ganglion-private#71](https://github.com/duke-of-beans/ganglion-private/pull/71) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-3198554a` **Effector writes live progress while a dispatch runs** (ganglion) — [duke-of-beans/ganglion-private#72](https://github.com/duke-of-beans/ganglion-private/pull/72) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-35a8ab3f` **Effector ends runs David kills** (ganglion) — [duke-of-beans/ganglion-private#70](https://github.com/duke-of-beans/ganglion-private/pull/70) · merged, checks green, deployed
- 2026-11-14 `wo-20261011-68863323` **Self-hosted GitHub Actions runner on Sentinel for the work-order gate (stop paying for Actions minutes)** (ganglion) — [duke-of-beans/easter-agency#23](https://github.com/duke-of-beans/easter-agency/pull/23), [duke-of-beans/ganglion-private#57](https://github.com/duke-of-beans/ganglion-private/pull/57) · merged; David accepted it as is despite: duke-of-beans/ganglion-private#57 checks failed (gate)
- 2026-11-13 `wo-20261011-8a2f8319` **Land greg-backend self-hosted gate + CI workflow PR (#44)** (ganglion) — [duke-of-beans/ops-context#34](https://github.com/duke-of-beans/ops-context/pull/34) · merged, checks green

<!-- work-orders:recorded wo-20261011-68863323 wo-20261011-8a2f8319 wo-20261115-0fdda381 wo-20261115-182038b2 wo-20261115-3198554a wo-20261115-35a8ab3f wo-20261115-6a635cd0 wo-20261115-f160b884 wo-20261117-0741f7d4 wo-20261117-542aaf69 wo-20261117-59d77b1f wo-20261117-5cf5d07b wo-20261117-64f09cd8 wo-20261117-876b99fb wo-20261117-91a2e289 wo-20261117-9c58bd1c wo-20261117-a5a5a4ad wo-20261117-b22f7044 wo-20261117-c519c2a6 wo-20261117-c5b5e72a wo-20261117-c85d4a83 wo-20261117-e8899da2 wo-20261117-eec95b81 wo-20261117-ffa284d3 wo-20261117-fff1fd95 -->
<!-- work-orders:end -->
