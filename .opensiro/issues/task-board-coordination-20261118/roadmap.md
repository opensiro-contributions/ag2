# AG2 — Wave 4 post-v0.18.0 neutral independent roadmap receipt (2026-11-20)

Same stable fork-local case `task-board-coordination-20261118`; **fresh independent** architectural sufficiency decision, preserved historic NO_GO in Git ancestry.

## Identity and pins

- Original repository: ag2ai/ag2
- Original HEAD: 6d2dd8bab8af873ea29ed759cfacb572466d925e
- Observed at: 2026-11-20
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/dadcf25d6e7ffcbdb298e476a249b8be187c53b4/assessments/ag/ag2.md
- Accepted assessment blob SHA: cc442691abb833236f48f30206580bb17c258f5c
- Accepted review ref: 3211bb19832049e7abe1a5742b6d177274bff723
- Accepted reviewed at: 2026-09-18
- Profile version: 0.2.2
- Assessment procedure version: 0.3.1
- Original default branch: main
- Published Upstream protocol: https://github.com/opensiro/upstream/commit/28ea2cce06b517bc4550dceddb00210b1e0dc85c
- System in focus: First-party AG2 v1 Agent and optional Network Hub channels at one Network boundary; excludes AG2 Classic, downstream client schedulers, tenant S5, repository CI
- Receipt contract: proposal-gate
- Repository-wide source map: Pinned README, AGENTS.md, ag2/agent.py, ag2/task.py, ag2/network/hub/core.py and arbiter.py, client/agent_client.py, task_mirror.py, adapters/discussion.py and workflow.py, transitions.py, network docs, test roots, contributor AI policy, original Issue 3679, original PRs 3576 2775 3128 and 3466
- Priority rationale: Only S3 has a source-grounded missing function-specific management decision with a feasible original-native agent/Hub/Task effect-and-return constructor. S1 autonomous and S2 first-party C already; S3* independent audit and S4 prospective future loop have no stronger reviewed P0; S5 reserved to parent.
- Accepted VSM vector: S1=A · S2=C · S3=— · S3*=— · S4=— · S5=—
- S1 disposition: ALREADY_A — Agent model/tool action and observation loop exists; do not duplicate operating agency
- S2 disposition: ALREADY_C — first-party DiscussionAdapter regulates turn sequence; WorkflowAdapter supplies scripted dispatch rather than organizational S3 choice
- S3 disposition: P0_C_HYPOTHESIS — agent-owned Task and observe-only Hub lack shipped cross-worker current priority decision owner; optional lawful function-specific manager is constructible
- S3* disposition: NOT_SELECTED — TaskMirror HubListener and audit are observations, not a proven independent complementary corrective audit owner
- S4 disposition: NOT_SELECTED — present provider configuration does not itself establish prospective external intelligence decision and effect/feedback
- S5 disposition: PARENT_RESERVED — human/tenant retains purposes permissions identity and final product/approval decisions
- Target transition: S3=— -> S3=C
- P1 dependencies: Lawful coordinator scope, revisioned shared assignments, worker-owned Task lifecycle protection, targeted dispatch, returned terminal correlation, crash/replay/remote-mode tests, static/Issue-3679 baseline
- P2 optional: NONE
- Proposed C construction: Opt-in source-native Network current-control manager, developer-composed S3 decision owner choosing among whole-workload assign defer reprioritize hold release; versioned authorized targeted AgentClient dispatch and TaskMirror/Hub feedback changing the subsequent decision
- C sufficiency falsifier: An equivalent first-party whole-network shared-priority S3 decision and return loop is already shipped at this recursion boundary, or no lawful versioned dispatch and Task-owned return can close the proposed actor
- Scenario basis: HYPOTHETICAL
- Proposal-stage decision: GO
- Research disposition: NEEDS_EVIDENCE
- Proposed validation: NOT_RUN — four-agent source-native tests must verify two lawful manager alternatives, actual targeted effect, TaskMirror return, state revision and negative revoked-owner/stale/retry/remote cases against static routing and original Issue 3679
- Validation state: NOT_RUN
- Proposal falsifier: A replaying or unauthorised manager cannot change later allowed worker operations on real Task terminal feedback; or the same full S3 closure is proven already first-party
- Evaluation object: Same historical fork-local whole-Network S3 current-priority/capacity controller in Task/Network, distinguished from a narrow selective-next-wake only adapter
- Existing-work overlap: SHIPPED Task ownership/TaskMirror/Hub observe+list/targeted AgentClient/WorkflowAdapter; ISSUE_ONLY original #3679 board; MERGED #3576 #2775 #3128; OPEN_PR #3466 tool burst, not S3
- Our on-top contribution: Minimum opt-in first-party S3 current-control actor composition with revisioned shared commitments, lawful capacity/priority discretion, actual targeted assignment and returned work feedback; no default behavior/product code change
- Incremental benefit: HYPOTHETICAL developer ability to compose whole-Network current management rather than only next-only wake; task outcomes/correctness/total engineering cost are NOT_MEASURED
- Decision scope: GO to structurally sufficient source-native S3=C proposal, not AG2 product adoption, not automatic Index regrade, not a verdict on Issue 3679, not permission to implement or publish

## Rights and authority

- Verified original Apache-2.0 license and [first-party AI policy](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/.github/AI_POLICY.md); any future external AG2 code PR must pass original CLA/maintainer requirements.
- Verified matching working fork `opensiro-contributions/ag2` is a real fork of `ag2ai/ag2`. Fork metadata branch `opensiro/meta` state `ACTIVE/ALLOW` before this write, allowing only OpenSiro internal .opensiro record maintenance.
- Task owner S1 actor keeps Task lifecycle and cancellation; proposed S3 manager must use explicit tenant/parent permission. S5 identity, application purpose, actual adoption, source code, original/fork public GitHub Issues/PRs and all third-party communications are not delegated by this record.

## Existing work / overlap

- [Original Task agent ownership](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/task.py), [Hub observe/list](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/core.py), [TaskMirror](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/task_mirror.py), [HubClient](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/client/hub_client.py), [AgentClient](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/client/agent_client.py), [HubArbiter](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/network/hub/arbiter.py).
- [Original #3679](https://github.com/ag2ai/ag2/issues/3679) OPEN (owner's desired selective-wake board, **not** a shipped network S3 actor); original [PR #3576](https://github.com/ag2ai/ag2/pull/3576), [#2775](https://github.com/ag2ai/ag2/pull/2775), [#3128](https://github.com/ag2ai/ag2/pull/3128) MERGED; [#3466](https://github.com/ag2ai/ag2/pull/3466) OPEN @81aef1444d0e55ae242591b6b4fae2e43b294599 and scoped to per-response concurrent tools.
- No current production implementation, quantitative utility benchmark or equivalent function-specific cross-worker managerial ownership claimed.

## Function ownership

- S1 agent owns selected tool/model work and task terminals; first-party S2 channels serialize inter-agent turns.
- Proposed S3 manager is a developer-composed function-specific decision owner, not merely the Hub observer or deterministic router: chooses shared workload priority/capacity actions within tenant authority, changes which S1 starts work, and receives next Task result to revise subsequent choice.
- S3* observation is not promoted to independent audit; S4 missing prospective loop is not presumed a defect; S5 remains parent-reserved. No simultaneous six-function upgrades.

## Capability priority

- P0: S3=— -> S3=C — source-native optional full S3 current-control path with manager decision, versioned shared work, authorized downstream assignment and closed returned feedback
- P1: Validate same-boundary rights, transactional/idempotent assignment and real AgentClient/Hub/TaskMirror round trip; compare static native targeted routing and #3679 board at equal functional task
- P2: NONE
- Current project action: research/design only; separate original product implementation decision belongs to AG2 maintainers

## Parallel contribution-on-top review

- Track A: Shipped Task/Hub/Network event, coordination and enforcement primitives already cover per-task lifecycle, scripted turn choice, targeted send and status observations. Original #3679 may solve narrow wake/noise with less engineering.
- Track B: Proposed opt-in whole-network **S3 organizational** decision right for multiple work commitments under changing capacity/priority, not another user-notification field. Only the delta to owner choice and enforceable feedback is included.
- Same historical evaluation object: [2026-11-19 immutable NO_GO@f33ff627](https://github.com/opensiro-contributions/ag2/blob/f33ff627c9d9b405c914ec78e63fc28d04f96282/.opensiro/issues/task-board-coordination-20261118/roadmap.md) rejected additional S3 on demand/novelty grounds. Fresh independent [v0.18.0 result sealed first](https://github.com/opensiro/upstream/issues/58#issuecomment-7042841496) admits GO for coherent constructibility while retaining NEEDS_EVIDENCE for empirical need, economics, tests and adoption. Narrow next-wake adapter is not S3 sufficient by itself; history is not deleted.

## Implementation options

- P0 alternative A: original-native optional manager class + approved task ledger, using existing HubClient and AgentClient dispatch with TaskMirror returned terminal.
- Comparator B: tenant-owned next-only routing or original Issue #3679 TaskBoard; valid engineering alternatives, not proof of equivalent whole-current S3 closure.
- Stop if parent authority is missing, source forbids a supported effect, original first-party equivalent S3 already closes, or tests falsify real feedback. Do not bypass Task owner semantics.

## Specification and domain alternatives

- No independent Profile/Skills change indicated by this single proposal; independent Index reassessment would be the only way to publish new actual S3 grade after implementation.
- No new mandatory S3*/S4/S5 target, domain-specific fork implementation or external project Issue recommended by the present research. Maintainer preference NOT_STATED.

## Cost experiment

- Cost status: NOT_MEASURED
- Future fair benchmark: same four-worker workload across static native routing, original #3679 board (if available) and composed S3 manager; compare terminal correctness, wakeups, tokens, duration, source integration, review, authorization/security tests, maintenance cost and stale/replay recovery. No cost or utility result inferred.

## Delivery and publication

- Result: NEEDS_EVIDENCE
- External issue: DRAFT — NOT PUBLISHED
- Human issue: [issue.md](issue.md)
- AI constructor: [constructor-sufficiency.md](constructor-sufficiency.md)
- Independent first-pass checkpoint: https://github.com/opensiro/upstream/issues/58#issuecomment-7042841496
- Fork-local storage: same stable case ID in `opensiro/meta`, historical evidence retained by Git lineage
- Native tests: NOT_RUN
- Economic comparison: NOT_MEASURED
- Product implementation: NOT_IMPLEMENTED
- Index grade: UNCHANGED
- Fork public GitHub Issue: NOT_PUBLISHED
- Original third-party communications: NOT_PUBLISHED
- Next permitted step: internal operator review of structurally sufficient design, future independent native tests and separate exact approval if any public Issue or maintainer interaction is requested
