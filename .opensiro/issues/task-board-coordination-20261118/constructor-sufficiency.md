# AG2 — S3=C optional Network current-management constructor (AI/developer)

**PLAN_ONLY · PROPOSAL GO / NEEDS_EVIDENCE · NOT IMPLEMENTED · NOT PUBLISHED**

**Target transition:** S3=— -> S3=C
**Proposal-stage decision:** GO
**Research disposition:** NEEDS_EVIDENCE

**Human decision:** [issue.md](issue.md).
**Canonical source-pinned six-function dispositions, P0/P1/P2 and verdict:** [roadmap.md](roadmap.md). The accepted vector is historical and unchanged; this file is the technical *construction* contract, not a second Index assessment.

## 1. Original-native boundary, rights and source evidence

AG2 v1 `ag2.Agent` with optional `ag2.network` Hub and channels on original `main@6d2dd8bab8af873ea29ed759cfacb572466d925e`. Exclude AG2 Classic, external scheduling implementations, general repository CI and the parent's S5. The accepted `included` assessment [Index@dadcf25d6e7ffcbdb298e476a249b8be187c53b4](https://github.com/opensiro/vsm-harness-index/blob/dadcf25d6e7ffcbdb298e476a249b8be187c53b4/assessments/ag/ag2.md) supplies historical grade, not modern implementation proof. Task owners remain separate S1 units. The opt-in composed manager holds only explicit application/tenant-delegated allocation rights; Hub task mutation ownership restrictions and parent policy remain in force.

Relevant current source: [Task](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/task.py) explicitly does not schedule/assign; [Hub.observe_task/list_tasks](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/core.py) observes current ownership, does not execute Agent.ask or assign; [TaskMirror](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/task_mirror.py) forwards owner lifecycle observations; [AgentClient](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/client/agent_client.py) can open targeted channels and emit envelopes; [HubArbiter](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/arbiter.py) provides pre-commit deny/allow, not organizational manager itself; [WorkflowAdapter](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/adapters/workflow.py) resolves scripted next turns, not independent cross-task priority.

## 2. Track A native first, Track B minimum on top

| Required function-specific S3 link | Track A source/current status | Track B minimum source-native extension | Stop/falsifier |
| --- | --- | --- | --- |
| Current view of shared commitments and worker availability | SHIPPED `TaskMetadata`, `Hub.list_tasks`, `Resume.observed`, rules | Revisioned, replay-safe work-item/assignment ledger with parent-allowed worker/capacity view | No lawful shared boundary or existing equivalent S3 current manager |
| Organizational decision owner with alternative lawful actions | SHIPPED agent S1 loops, `AgentClient.open`, `HubArbiter` | Opt-in developer-composable S3 decision actor choosing `assign/defer/hold/reprioritize/release` over multiple worker commitments | Only static next-message routing or no choice independent of transport |
| Enforced effect on **later** work | SHIPPED targeted envelope/channel dispatch with Hub enforcement | Versioned selected worker activation and atomic claim with explicit manager rights; fail closed on denial | Remote mode unsupported, unauthorized cross-owner Task mutation needed |
| Return/correction | SHIPPED Task terminal events, mirror, Hub store | Correlate assignment ID/revision to Task terminal (or timeout/failure), deduplicate, update later prioritized commitment and re-decide | Only logs/notifications with no decision feedback |

**Track A original-native comparator:** [Issue #3679](https://github.com/ag2ai/ag2/issues/3679) is open request for a board and single-next wake; no shipped board was observed. [#3576](https://github.com/ag2ai/ag2/pull/3576), [#2775](https://github.com/ag2ai/ag2/pull/2775), [#3128](https://github.com/ag2ai/ag2/pull/3128) merged Task/Network/governance pieces; [#3466](https://github.com/ag2ai/ag2/pull/3466) OPEN @81aef1444d0e55ae242591b6b4fae2e43b294599 handles concurrent tool calls *inside one batch*, not cross-worker whole-current management. A simpler host-owned next wake may fully satisfy the original *narrow feature request*, but it does not establish an equivalent S3 owner and feedback loop.

**On-top distinctness:** choose a *different evaluation object from mere selective wake*: current **organizational priority/capacity** control across worker Tasks. A coherent native first-party constructor lets developer supply the manager's policy/actor while the framework supplies safe claim/dispatch/return. This is not a mandatory new daemon; implementation may be an opt-in class + adapter and tests.

## 3. Minimum construct and actor-effect-feedback wiring (proposed, not shipped)

1. **Read and authorize.** The manager receives a bounded, versioned snapshot of `TaskMetadata`, currently eligible workers, capacity/queue thresholds and parent-granted action scope. Never infer authority from visibility or falsely claim an existing Hub API assigns tasks.
2. **Decide.** A developer-composed decision owner chooses among at least two feasible whole-current alternatives, e.g. queue task B behind a busy worker or delegate task B to idle worker C, with reason and expected revision. Owner is function-specific S3, not merely `WorkflowAdapter` transport.
3. **Commit effect.** The optional first-party manager atomically claims one work item, verifies authority/recipient and emits *one* targeted task instruction over existing AgentClient/HubClient paths. Agent-owned `Task` creation and terminal marking stay on the recipient, not manager. HubArbiter denies out-of-scope sends; on denial no assignment is committed as effective.
4. **Return and correct.** Match TaskStarted/Progress/Completed/Failed/Cancelled/Expired from TaskMirror/Hub by assignment revision, with timeout and idempotent replay. Update prioritized commitments then cause the manager to select a subsequent lawful alternative. A static `next` field or audit listener by itself fails here.
5. **Recursion/stop.** All work remains within one parent-authorized AG2 Network. User/tenant retains purpose, policy, human approvals and the option not to enable the manager. Fail closed on revoked authority, stale state, missing result or remote transport uncertainty; no new S5 or task-owner impersonation.

**Counterfactual:** without the composed manager and its revisioned decision/effect/feedback glue, existing Hub can observe Tasks and route scripted turns, but does not make an independently specified organization-wide priority allocation on new terminal feedback. Therefore a first-party C constructor remains structurally possible; future implementation/validation and Index grade are separate.

## 4. Decision, prerequisites and exclusions

**P0:** source-native optional `S3=— -> S3=C` constructor, using current Task/Hub/AgentClient/TaskMirror rather than reimplementing them. **P1:** worker consent/authority matrix, safe serialization and cross-process semantics, actual dispatch-return integration, frozen native tests and matched simpler alternative. **P2:** NONE.

Do **not** create a second selective-wake adapter merely because #3679 is open; do **not** implement S3*, S4, S5 or alter default AG2 behavior. Independently verify whether native composable policy already closes exact S3 prior to engineering.

## 5. Proposed native acceptance and falsification (NOT_RUN)

Existing first-party test roots are [test/network](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/test/network) and [test/test_task.py](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/test/test_task.py); command proposal is `python -m pytest test/network test/test_task.py`, **NOT_RUN** (no AG2 code change/test environment executed). Proposed tests must be added to the original native suite before any implementation claim:

- Positive: two registered workers and a manager with valid parent scope; one full-current priority decision causes exactly one authorized targeted worker execution, Task result returns through TaskMirror, and next decision changes based on returned state.
- Alternative: under equal inputs choose defer vs assign, both lawful outcomes and their real later operations observable; proves decision ownership rather than a hardcoded router.
- Negative: revoked manager scope, worker refusal, stale ledger revision, duplicate event, reconnection, missing Task terminal and a parent STOP must not cause unapproved or duplicate execution, forged Task status or lost receipt.
- Comparator: same deterministic four-agent workflow with existing host-specific next wake and original #3679 minimal board if shipped. Compare correctness and engineering/maintenance cost *after* evidence exists. Costs and time savings NOT_MEASURED.

**Design falsifier:** same function-specific first-party cross-worker S3 decision ownership already exists, or no lawful effect+closed feedback can be constructed in supported AG2 modes. More economical native routing may be chosen by maintainers but is a distinct product decision.

## 6. Historical difference and publication gate

This post-v0.18.0 source-first decision was written before historic read in [#58 checkpoint](https://github.com/opensiro/upstream/issues/58#issuecomment-7042841496). The earlier [receipt@f33ff627](https://github.com/opensiro-contributions/ag2/blob/f33ff627c9d9b405c914ec78e63fc28d04f96282/.opensiro/issues/task-board-coordination-20261118/roadmap.md) returned NO_GO mainly for unproven separate utility versus #3679; the newly published neutral protocol accepts a complete construction without prior benefit proof or adoption preference. Same S3-manager object: old NO_GO → this proposal GO; narrower next-wake adapter alone remains S3-incomplete. Stored history stays immutable.

**Proposal-stage decision:** GO. **Research:** NEEDS_EVIDENCE. **Native test state:** NOT_RUN. **Cost:** NOT_MEASURED. **Public GitHub Issue:** DRAFT — NOT PUBLISHED; external original communications and product implementation require exact consent and native review. [Human Issue](issue.md) and [canonical roadmap](roadmap.md) are the only handoff surfaces.
