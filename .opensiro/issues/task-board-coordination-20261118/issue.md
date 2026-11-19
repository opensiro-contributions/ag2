# AG2 — independent Task/Network on-top rerun (Human)

**PLAN_ONLY · proposal-stage NO_GO · research NO_USEFUL_CHANGE · internal .opensiro sync, NOT PUBLISHED.**

**Target transition:** NO_QUALIFIED_C_TARGET
**Proposal-stage decision:** NO_GO
**Research disposition:** NO_USEFUL_CHANGE

[roadmap.md](roadmap.md) · [constructor-sufficiency.md](constructor-sufficiency.md)

## Why OpenSiro and historic accepted assessment

OpenSiro tests whether VSM-informed function-specific integration can lower the real task engineering burden; benefit is a falsifiable hypothesis, not a defect attributed to AG2.

[Included Index assessment](https://github.com/opensiro/vsm-harness-index/blob/9fe281441f1820014dda5da8fff70e5fb1c9b246/assessments/ag/ag2.md) for AG2, blob cc442691abb833236f48f30206580bb17c258f5c, reviewed 2026-09-18 at 3211bb19832049e7abe1a5742b6d177274bff723 under Profile 0.2.2 and methodology 0.3.1; original examined at [6d2dd8bab8af873ea29ed759cfacb572466d925e](https://github.com/ag2ai/ag2/commit/6d2dd8bab8af873ea29ed759cfacb572466d925e). The accepted state is historical and is not reassessed by this sync.

| Function and plain meaning | Historical accepted state | Source ownership and why not chosen |
| --- | --- | --- |
| **S1 · Operations** | A | Agents autonomously perform model/tool work and return Task results. No new C required |
| **S2 · Coordination** | C | Network discussion already supplies composable turn regulation and feedback; one-next board is an original native feature discussion |
| **S3 · Current management** | — | No current independent resource/priority controller is established, but no evidenced distinct extra operator need beyond host-targeted Task routing and #3679 |
| **S3* · Complementary audit** | — | TaskMirror/events are not an independent corrective audit owner |
| **S4 · Prospective adaptation** | — | No sourced external-future decision/return target |
| **S5 · Identity/policy** | — | Parent/developer controls authority; no new identity actor justified |

## Operator task

The observed request in [original Issue #3679](https://github.com/ag2ai/ag2/issues/3679) is that a four-agent pipeline wakes ONLY its next relevant agent rather than every participant, while preserving correct terminal Task ownership and avoiding unneeded tokens. This is legitimate native work. It does **not** imply another fully autonomous VSM S3 controller is useful. The easiest alternative is application-owned targeted dispatch using existing Hub/Task primitives.

## Original-native Track A and independent Track B

| Track A | Track B / cheapest additional work | Result |
| --- | --- | --- |
| [Task](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/task.py) agent-owned events and checkpoints; Network targeted delivery, TaskMirror; original #3679 already asks for board and next wake | Reuse targeted host routing or help original owner's board with terminal-safe Task receipts | Not an independent S3 construction |
| Merged original [#3576](https://github.com/ag2ai/ag2/pull/3576), [#2775](https://github.com/ag2ai/ag2/pull/2775), [#3128](https://github.com/ag2ai/ag2/pull/3128); open [#3466](https://github.com/ag2ai/ag2/pull/3466) governs per-response tool bursts | Optional distributed revisioned/idempotent wake adapter | No observed wrong/lost/double wake remaining after native options; NOT_EVIDENCED |
| Original #3679 four-agent benchmark proposed | Compare unchanged host targeting, minimal board and only then conditional adapter | Native counterfactual must fail before another first-party constructor is justified |

## Priority and independent decision

**P0:** NO_QUALIFIED_C_TARGET — scoped NO_GO for separate whole-network S3=C managerial service or duplicate one-next adapter.

**P1:** Native owner-led issue #3679; benchmark selective wake, correct Task terminals, unauthorized/stale/duplicate wake and total operating/engineering cost.

**P2:** NONE.

A real S3=C proposal would need whole-current commitments snapshot, independently developer-composed autonomous decision owner, lawful alternative actions, enforced dispatch and later Task feedback. The missing historical grade is not evidence those new parts would help this use case.

**Falsifier and reentry:** An actual cross-process double/lost wake not addressed by targeted native handlers and the minimal original board, plus a testable distinct organizational controller need, could justify reconsideration. No new code or benchmark was executed in the independent study.

## Rights, chronology and delivery

[Source comment for independent 2026-11-19 review](https://github.com/opensiro/upstream/issues/58#issuecomment-7012239664) reported NO_GO and READ_ONLY because the then-fork owner state was PAUSE/DORMANT. The owner has since switched this matching fork to ACTIVE/ALLOW, enabling **this internal-only synchronization**. The preceding 2026-11-18 research remains in Git history, not overwritten as a claimed fresh assessment. No original-project or public-fork Issue/PR approved, no Index grades changed.

[Canonical receipt](roadmap.md) and [AI handoff](constructor-sufficiency.md) keep exact pins, tests and publication/authority limits.
