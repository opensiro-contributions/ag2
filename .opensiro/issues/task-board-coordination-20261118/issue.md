# AG2 — task-board coordination roadmap (OpenSiro plan-only)

**Status:** PLAN_ONLY · architecture decision: **NO_GO for a separate VSM S3 constructor now** · public fork GitHub Issue: **NOT PUBLISHED**.

## Why OpenSiro

OpenSiro tests whether a reusable, VSM-informed organizational specification can standardize agent-harness development and lower its total implementation, integration, review and maintenance cost. This is an **unmeasured hypothesis**, not a statement that AG2 needs VSM or that cost savings are proven. Prefer a smaller original-native solution when it solves the real user task.

## Accepted VSM starting point — historical, not a current-HEAD grade

[Accepted Index assessment](https://github.com/opensiro/vsm-harness-index/blob/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f/assessments/ag/ag2.md), reviewed **2026-09-18**, original `review_ref` `3211bb19832049e7abe1a5742b6d177274bff723`, Profile **0.2.2**, Methodology **0.3.1**:

| Function | Grade | Meaning and assessment consequence |
| --- | --- | --- |
| S1 — Operations | **A** | The AG2 model/tool agent owns execution choices; no mandatory C work. |
| S2 — Coordination | **C** | The composable first-party Network discussion protocol regulates participant turns; no mandatory replacement. |
| S3 — Current control | **—** | A first-party whole-organization commitments/resources decision loop was not established at the reviewed ref. |
| S3* — Complementary audit | **—** | Hub logs and listeners did not establish an independent audit-return path. |
| S4 — Adaptation | **—** | No separate prospective environmental adaptation loop was established. |
| S5 — Policy and identity | **—** | Network governance remains developer/parent-defined rather than autonomously closed. |

The original now has newer code at [`f3943efb5546c4dbaecaf08706eb2bc16e56c602`](https://github.com/ag2ai/ag2/commit/f3943efb5546c4dbaecaf08706eb2bc16e56c602); this vector is **historical**. Because the last accepted review was over 30 days ago, recommend a source-pinned Index re-assessment before asserting any current grade change. Re-assessment is advisory, not a roadmap blocking gate.

## Real user outcome and native work

[AG2 issue #3679](https://github.com/ag2ai/ag2/issues/3679) requests a shared task board that wakes only the agent named `next`, avoiding irrelevant agent invocations and context delivery. AG2 currently supplies a [per-agent Task lifecycle](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/ag2/task.py) and [Task documentation](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/website/docs/user-guide/tasks.mdx) that expressly leave task assignment/scheduling to owners. [PR #3576](https://github.com/ag2ai/ag2/pull/3576) was merged and unified task lifecycle; [PR #3466](https://github.com/ag2ai/ag2/pull/3466) is still open on per-batch tool concurrency, **not** a cross-agent board. No board implementation or independent S3 actor has been established by this investigation.

A task board's `next` field and deterministic wake-up alone are **not** autonomous S3 current control: they do not establish who lawfully chooses cross-agent priorities/capacity, how that choice changes later agent work, or how feedback returns. Nor does absence of historical S3 force a new feature.

## Priority and minimum sufficient decision

- **P0 — NOT ADMITTED:** Do **not** open a separate VSM S3=C controller implementation. Current evidence establishes a concrete coordination-efficiency request, but not a distinct whole-organization S3 decision need. Proposed C ports in the [AI/developer contract](constructor-sufficiency.md) remain an unapproved hypothesis.
- **P1 — original-native route:** Reuse **#3679**, not a duplicate original Issue. Before any implementation mandate, compare a fixed four-agent pipeline using current Task+Network versus board+single-`next` dispatch. Count unnecessary wake-ups, model tokens, correct terminal task outcomes and total maintenance effort. Preserve existing agent ownership, auth, events and cancellation. A measured win could justify a small AG2-native board proposal independently of VSM grades.
- **P2 — NONE:** No separate S3*, S4, S5 or parent-autonomy mode is proposed without a new material first-party need.

**Minimum passing native result if the maintainer selects #3679 later:** exact one-agent wake behavior, no unrelated listener wake, authorization-safe transition, correct cancellation/terminal receipts, no regression in ordinary Task runs, and a reproducible baseline comparison. These tests are **proposed, not executed**. The user task may be delivered with no S3 grade change.

## Independent choices and limits

1. **Original-native:** Reuse #3679 and maintainer decisions; do not publish a competing Issue/PR automatically.
2. **Profile/Skills feedback:** Only if actual source evidence demonstrates a misclassified function or unclear threshold; no proposed semantic change now.
3. **Optional domain fork:** A separately authorized, bounded board+manager experiment only if a real cross-agent discretionary-control task emerges and a simpler native alternative fails.

AG2 is Apache-2.0. Its [AI contribution policy](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/.github/AI_POLICY.md) welcomes reviewed AI assistance and requires a contributor to certify PR rights under its CLA; no personal CLA consent is presumed. This plan publishes no code or message to AG2.

## Cost and final decision

**Cost: NOT_MEASURED.** Match implementation, integration, testing, review, token and maintenance cost for equivalent outcomes before claiming savings.

**Final decision: NO_GO** for a *separate VSM-derived S3 controller now*. **Next:** keep source-native #3679 as the sole original-project lead; re-evaluate only if measured benefit and a genuine autonomous whole-system priority/capacity decision need emerge. This is a closed research verdict, not `NEEDS_EVIDENCE` awaiting another generic continuation.

**Fork-local case:** [README](README.md) · [AI/developer evidence and constructor sufficiency](constructor-sufficiency.md) · [pinned receipt](roadmap.md). Product code: unchanged. Public fork GitHub Issue: **NOT PUBLISHED — requires separate exact current-conversation approval**. Original Issue/PR: **NOT PUBLISHED by OpenSiro**.
