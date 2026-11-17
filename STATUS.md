# GANGLION — STATUS

Status: infra
Last Updated: 2026-11-17
Last Recorded: wo-20261117-b22f7044 — Effector: scratch off tmpfs, per-dispatch TMPDIR, write gate, empty output fails

<!-- work-orders:begin (generated from portfolio.orders by the record step; edits inside this block are overwritten) -->
## Work orders

_Generated 2026-11-17T20:17:58.018Z from the work-order store. Done means verified and recorded; the live view is GregLite._

**Project:** ganglion (GANGLION, infra)

### Waiting on David

Nothing.

### In flight

| Order | Project | State | Title | Updated |
|---|---|---|---|---|
| `wo-20261117-e8899da2` | ganglion | dispatched | Loop-safe admission and one-output-per-cause for chained dispatches (from slack-agent-mesh) | 2026-11-17 |
| `wo-20261117-0741f7d4` | ganglion | drafted | Preview links: an agent builds an app on Sentinel, David gets a gated link (orgo-deploy pattern) | 2026-11-17 |
| `wo-20261117-c5b5e72a` | ganglion | drafted | Lane rules: one writer per checkout, self-reports aren't evidence, usage-limit means unavailable until reset | 2026-11-17 |
| `wo-20261117-5ed6543d` | ganglion | drafted | Effector CLIs start with an empty env; read-back output is scrubbed of key shapes | 2026-11-17 |
| `wo-20261117-91a2e289` | ganglion | drafted | Bake-off Qwen4-Max vs Kimi for the OpenCode lane, swap if it wins | 2026-11-17 |
| `wo-20261106-a8af50fa` | ganglion | drafted | Trim OpenCode prompt weight per GANGLION dispatch | 2026-11-06 |

### Receipts

None.

### Open kickbacks

None.

### Recently recorded (last 30 days)

- 2026-11-17 `wo-20261117-b22f7044` **Effector: scratch off tmpfs, per-dispatch TMPDIR, write gate, empty output fails** (ganglion) — [duke-of-beans/ganglion-private#76](https://github.com/duke-of-beans/ganglion-private/pull/76) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-182038b2` **Yokoten: environment fix from gregore** (ganglion) — [duke-of-beans/ganglion#24](https://github.com/duke-of-beans/ganglion/pull/24) · merged, checks green
- 2026-11-15 `wo-20261115-6a635cd0` **MAX usage sign-in without a terminal (Sentinel reader)** (ganglion) — [duke-of-beans/ganglion-private#74](https://github.com/duke-of-beans/ganglion-private/pull/74), [duke-of-beans/Gregore-private#904](https://github.com/duke-of-beans/Gregore-private/pull/904) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-0fdda381` **MAX plan usage reader on Sentinel** (ganglion) — [duke-of-beans/ganglion-private#73](https://github.com/duke-of-beans/ganglion-private/pull/73) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-f160b884` **OpenCode lane: allow harmless shell glue so runs aren't killed** (ganglion) — [duke-of-beans/ganglion-private#71](https://github.com/duke-of-beans/ganglion-private/pull/71) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-3198554a` **Effector writes live progress while a dispatch runs** (ganglion) — [duke-of-beans/ganglion-private#72](https://github.com/duke-of-beans/ganglion-private/pull/72) · merged, checks green, deployed
- 2026-11-15 `wo-20261115-35a8ab3f` **Effector ends runs David kills** (ganglion) — [duke-of-beans/ganglion-private#70](https://github.com/duke-of-beans/ganglion-private/pull/70) · merged, checks green, deployed
- 2026-11-14 `wo-20261011-68863323` **Self-hosted GitHub Actions runner on Sentinel for the work-order gate (stop paying for Actions minutes)** (ganglion) — [duke-of-beans/easter-agency#23](https://github.com/duke-of-beans/easter-agency/pull/23), [duke-of-beans/ganglion-private#57](https://github.com/duke-of-beans/ganglion-private/pull/57) · merged; David accepted it as is despite: duke-of-beans/ganglion-private#57 checks failed (gate)
- 2026-11-13 `wo-20261011-8a2f8319` **Land greg-backend self-hosted gate + CI workflow PR (#44)** (ganglion) — [duke-of-beans/ops-context#34](https://github.com/duke-of-beans/ops-context/pull/34) · merged, checks green

<!-- work-orders:recorded wo-20261011-68863323 wo-20261011-8a2f8319 wo-20261115-0fdda381 wo-20261115-182038b2 wo-20261115-3198554a wo-20261115-35a8ab3f wo-20261115-6a635cd0 wo-20261115-f160b884 wo-20261117-b22f7044 -->
<!-- work-orders:end -->
