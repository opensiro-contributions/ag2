# AG2 — optional source-native network-level S3 current-control constructor (Human)

**PLAN_ONLY · Wave 4 post-release v0.18.0 · GO / NEEDS_EVIDENCE · NOT IMPLEMENTED · NOT PUBLISHED**

**Target transition:** S3=— -> S3=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

[roadmap.md](roadmap.md) · [constructor-sufficiency.md](constructor-sufficiency.md)

## 1. Why OpenSiro and original developer outcome

OpenSiro tests the hypothesis that a reusable VSM-informed, function-specific construction could lower total harness engineering, integration and maintenance cost. This is **not** measured benefit, criticism of AG2, or an instruction to its maintainers.

**Proposed developer capability:** opt into a manager for a bounded AG2 Network which observes the current shared commitments of multiple workers and chooses which *lawful* work to allocate, defer, release or reprioritize next. The chosen Agent receives only its authorized work and returns Task outcome evidence to the same manager before another decision. A single-next-wake task board without authority, effect and return feedback is insufficient.

**System in focus:** AG2 v1 first-party `Agent` and optional Network Hub/channel runtime at [original main@6d2dd8bab8af873ea29ed759cfacb572466d925e](https://github.com/ag2ai/ag2/commit/6d2dd8bab8af873ea29ed759cfacb572466d925e). Exclude AG2 Classic, separate applications, downstream schedulers, and repository CI. Parent/user retain task-purpose, authority grant, privacy and publication rights. This is one Network recursion level, not a grant to create a new parent S5.

## 2. Six-function source-first screen and historical boundary

The [accepted included Index assessment](https://github.com/opensiro/vsm-harness-index/blob/dadcf25d6e7ffcbdb298e476a249b8be187c53b4/assessments/ag/ag2.md) is pinned to 2026-09-18 review `3211bb19832049e7abe1a5742b6d177274bff723` and Profile 0.2.2 / assessment procedure 0.3.1. Historical grades are **not changed** by this proposed construction.

| Function and why this target was or was not selected | Historical state | Current source-informed disposition |
| --- | --- | --- |
| **S1 · Operations** | A | [Agent](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/agent.py ) runs model/tool action loops and receives results; no mandatory C addition |
| **S2 · Coordination** | C | [DiscussionAdapter](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/adapters/discussion.py) enforces turn order; [WorkflowAdapter](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/adapters/workflow.py) routes fixed turns, not whole-workload S3 |
| **S3 · Inside-and-now** | — | **P0 eligible:** [Task](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/task.py) is explicitly agent-owned and Hub [core](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/core.py) observes tasks but does not assign/schedule them; no shipped whole-Network reprioritizing owner demonstrated |
| **S3* · Complementary audit** | — | [TaskMirror](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/task_mirror.py), logs and HubListener report events; not an independent corrective audit decision owner |
| **S4 · Future environment** | — | Model/provider choice and observation do not themselves form a first-party prospective external-adaptation and returned-action loop; no S4 priority here |
| **S5 · Identity and policy** | — | Parent/user/tenant rules and [HubArbiter](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/arbiter.py) enforce bounded authorization but do not create autonomous parent purpose/identity |

No omission is called deliberate without a source statement. AG2 Classic is intentionally a different repository; that fact does not determine AG2's product direction.

## 3. Constructible hypothesis and native alternatives

**Scenario basis: HYPOTHETICAL for cross-worker priority/capacity decisions; OBSERVED for the narrower original #3679 wake/noise problem.** A network with several active worker Tasks may need to adjust priority after a failed task or a capacity change. The qualified S3 target requires a manager able to choose an alternative and change later work at the same organizational boundary.

**Track A (shipped):** [Task](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/task.py), [TaskMirror](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/task_mirror.py), [Hub.list_tasks / Hub rules](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/core.py), [AgentClient targeted channel operations](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/client/agent_client.py) and [HubArbiter](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/arbiter.py). [Original Issue #3679](https://github.com/ag2ai/ag2/issues/3679) is **OPEN / ISSUE_ONLY**, requesting an optional shared TaskBoard and next-only wake. [PR #3576](https://github.com/ag2ai/ag2/pull/3576), [#2775](https://github.com/ag2ai/ag2/pull/2775), and [#3128](https://github.com/ag2ai/ag2/pull/3128) are **MERGED**; [#3466](https://github.com/ag2ai/ag2/pull/3466) is **OPEN_PR** but concerns per-batch tool-call concurrency, not cross-worker priority authority. No production TaskBoard or equivalent autonomous S3 ownership was verified from the pinned source.

**Track B / P0 (to construct):** minimal opt-in first-party `NetworkCurrentManager` (illustrative name) with a durable revisioned work/commitment ledger, owner-approved capabilities, assign/defer/hold/reprioritize decisions, race-safe claim, authorized targeted dispatch to AgentClient, and TaskMirror/Hub-returned completion/failure feeding the *next* manager decision. Developer composes the manager decision actor/policy; no manager may cancel/reassign another Agent-owned Task merely by writing Hub metadata. Stop or request parent decision when an effect cannot lawfully reach the worker.

| C requirement | Present in AG2 | Missing optional first-party construction |
| --- | --- | --- |
| Whole-current commitments and competing lawful choices | Task metadata, Network registry, rules, terminal events | Aggregate versioned work queue and capacity/priority decision input |
| Decisive organizational owner and operational effect | Targeted HubClient/AgentClient calls and custom arbiter gates | Developer-composed bounded S3 manager issuing only authorized worker assignments |
| Feedback and correction | Agent-owned Task lifecycle and TaskMirror | Correlate assignment revision + Task result/failure, deduplicate retry and decide next work |

**Native comparator:** unchanged tenant-owned selective routing; the narrow #3679 board; standard WorkflowAdapter static turns. These may be simpler to adopt but do not automatically establish equivalent function-specific S3 whole-current priority closure. Product choice is AG2 maintainers' decision.

## 4. P0/P1/P2 and structural sufficiency

**P0:** smallest complete optional `S3=— -> S3=C` Network current-control constructor described above. A mere `next` field, observer, or transport adapter does not qualify.

**P1:** verify cross-process authority for targeted dispatch, no protected Task ownership bypass, atomic revisioned work claims, recoverable idempotent retry, returned terminal feedback, and comparison with the smallest native static-routing/#3679 route.

**P2:** NONE.

**Proposed C-sufficiency verdict:** PROPOSED_C_SUFFICIENT as a source-native design, **not** implemented or accepted Index grade. The manager can select among two legitimate whole-current options and affect subsequent work; without that composed owner the same S3 decision is absent. Legitimate current rights bound every action.

## 5. Prospective acceptance / failure conditions

**Future positive (NOT_RUN):** deterministic four-Agent research→write→review→integrate pipeline with an operator-approved manager; after one worker fails, observe an authorized manager decision `defer/reassign` vs `retry/release`, the actual single intended next worker invocation, owner-controlled Task completion, and a returned state revision that changes the following manager decision.

**Future negative (NOT_RUN):** revoked/absent coordinator authority, unauthorized recipient, stale status revision, duplicate terminal event, lost/replayed delivery or parent STOP must never create extra work or forge Task owner status. A static channel turn or log-only receipt is not C closure.

**Falsifier:** first-party AG2 already contains *equivalent* function-specific whole-network current decision ownership and returned organizational feedback, or the proposed bounded manager cannot lawfully cause and observe an effect. Lower-cost native solutions inform the adoption comparator but do not alone negate constructibility. Benefit and costs **NOT_MEASURED**.

## 6. Independent comparison to the historical decision (only AFTER new verdict)

New source-first six-function/Track A/B judgment was sealed in [Upstream #58 checkpoint](https://github.com/opensiro/upstream/issues/58#issuecomment-7042841496) **before** reading this case's older 2026-11-19 NO_GO. The old [immutable receipt@f33ff627](https://github.com/opensiro-contributions/ag2/blob/f33ff627c9d9b405c914ec78e63fc28d04f96282/.opensiro/issues/task-board-coordination-20261118/roadmap.md) rejected both a separate network-level S3 manager and duplicate selective-wake adapter because additional operator *need/benefit* over native #3679 had not been shown. Under published [v0.18.0 assessment neutrality](https://github.com/opensiro/upstream/blob/v0.18.0/PROTOCOL.md), absence of a demonstrated benefit or a maintainer preference is not a constructibility veto. **Same S3 manager evaluation object: old NO_GO → proposed GO; research NEEDS_EVIDENCE.** The *narrow wake-only adapter* remains insufficient for S3 and is not independently promoted to GO. History remains in Git ancestry.

## 7. Cost and integration decision

Current implementation, reviewer, integration, migration and ongoing maintenance effort are **NOT_MEASURED**. Future comparison must include current tenant-owned routing, original #3679 native board, and composed S3 manager at matched behavior, code/test volume, latency, tokens, crash recovery and governance/maintenance cost. AG2 maintainers alone choose adoption.

## 8. Rights, next permitted action and publication

Verified working fork `opensiro-contributions/ag2` has parent `ag2ai/ag2`; `opensiro/meta` control was **ACTIVE / ALLOW** at preflight, permitting internal metadata updates only. Original is Apache-2.0 with [AI policy](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/.github/AI_POLICY.md) and CLA for external contribution; neither those formalities nor external/public-fork issue publication is assumed approved.

**Decision:** GO; **Research:** NEEDS_EVIDENCE; **Validation:** NOT_RUN; **Cost:** NOT_MEASURED. Publish no fork public Issue, original comment/PR, source code or Index grade. The full draft is this Human text, awaiting distinct exact publication consent. [Technical contract](constructor-sufficiency.md) · [canonical receipt](roadmap.md).
