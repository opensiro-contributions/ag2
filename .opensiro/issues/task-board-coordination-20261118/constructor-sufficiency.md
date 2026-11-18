# AG2 — AI/developer evidence and conditional constructor contract

**Companion to:** [Human roadmap Issue](issue.md). **Status: PLAN_ONLY / NO_GO** for a separate S3=C intervention; no implementation authorization.

## Function scope, boundary and historical starting vector

System in focus: AG2 first-party Agent and opt-in Network Hub at [accepted Index ref](https://github.com/opensiro/vsm-harness-index/blob/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f/assessments/ag/ag2.md) `3211bb19832049e7abe1a5742b6d177274bff723`. Current original main: [`f3943efb5546c4dbaecaf08706eb2bc16e56c602`](https://github.com/ag2ai/ag2/commit/f3943efb5546c4dbaecaf08706eb2bc16e56c602).

**Accepted historical vector (2026-09-18): S1=A, S2=C, S3=—, S3*=—, S4=—, S5=—.** Profile 0.2.2; Methodology 0.3.1. S2=C is already a supported composable turn-regulation path; this route does **not** require its replacement. No source change/Issue upgrades the accepted assessment.

## 1. Real counterfactual and existing current code

Operator counterfactual from [original issue #3679](https://github.com/ag2ai/ag2/issues/3679): a four-agent pipeline should not invoke idle/non-next agents or send each the full status stream. The cheapest solution is to preserve agent-owned Tasks and supply a small optional single-next task board, not a new organization-level management service.

| First-party mechanism | Current provenance and status | Ownership conclusion |
| --- | --- | --- |
| `ag2/task.py` and Task docs | [Source at original HEAD](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/ag2/task.py); Tasks emit start/progress/terminal, checkpoint and are explicitly owner-scheduled | **SHIPPED** Task lifecycle, **not** shared task assignment |
| Ordinary and delegated Task lifecycle | [PR #3576](https://github.com/ag2ai/ag2/pull/3576) **MERGED** 2026-11-03 | Reuse existing receipts, do not recreate Task |
| Network Hub / protocols | [PR #2775](https://github.com/ag2ai/ag2/pull/2775) **MERGED**; [accepted S2=C evidence](https://github.com/opensiro/vsm-harness-index/blob/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f/assessments/ag/ag2.md) | Existing coordination and governance; **not** a proven first-party S3 controller |
| Shared board / single-next wake | [Issue #3679](https://github.com/ag2ai/ag2/issues/3679) **OPEN**, with no source-proven implementation in this check | **ISSUE ONLY**, not SHIPPED C |
| Concurrent tool-call cap | [PR #3466](https://github.com/ag2ai/ag2/pull/3466) **OPEN**, head `81aef1444d0e55ae242591b6b4fae2e43b294599` | Different per-agent tool pressure, not multi-agent task priorities |
| Deterministic governance middleware | [PR #3128](https://github.com/ag2ai/ag2/pull/3128) **MERGED** | Policy enforcement support, not an autonomous resource allocator |

Search for board/task scheduling PRs did not identify an accepted competing implementation. This bounded search is **not** a claim that every historical branch or downstream plugin has been tested. AG2 Classic is outside this AG2 v1 first-party boundary.

## 2. Conditional S3 C-target sufficiency (NOT ADMITTED)

A first-party `TaskBoard` as described in #3679 would improve task-level coordination, but `next` chosen by the caller is a deterministic dispatch parameter. To test **S3=C**, a *separate demonstrated user task* must require an organizational actor to decide current capacity, priority and commitments, not merely execute a configured queue. Only then could a first-party, developer-composable path expose the following complete chain:

| Logical port (conditional) | Required current-work decision and return | Existing vs missing |
| --- | --- | --- |
| **A: CurrentWorkSnapshot** | Observed cross-agent tasks, status, owner, commitments, capacity, revision and trust boundaries | Task events / Hub observations **SHIPPED** in part; coherent board scope **NOT SHIPPED** |
| **B: EligibleInterventions** | Versioned lawful choices: assign, defer, re-prioritize, hold, cancel, with quota and invariant checks | No first-party organization-level options demonstrated |
| **C: CurrentWorkDecisionPort** | Developer composes a real autonomous decision actor choosing among those options under valid delegated authority | **MISSING** S3-specific actor/decision contract |
| **D: DispatchAndAuthorityBridge** | Validate actor identity, revision, task ownership, resource rights and apply the chosen change to supported AG2 Task/Network dispatch | Task/Network execution **SHIPPED**; bound decision-to-actual-next-work bridge **MISSING** |
| **E: ActualWorkReceipt** | Evidence that the selected worker ran or was denied, changed later Task state and returned outcome to the same current controller | Task terminal events **SHIPPED**; organization-level controller feedback **MISSING** |

**Conditional sufficiency rule:** only the full native A+B+C+D+E path, actually implemented and tested in standard first-party modes, could be proposed for a later independent Index review of S3=C. An event hook, static `next`, paper contract, outsider worker, green mock test, or new Issue cannot establish C. Respect parent/developer policy, no new S5 rights. **Materiality gate fails now** because the independently useful whole-system discretionary choice has not been demonstrated.

## 3. Priorities identical to Human decision

- **P0: NOT ADMITTED** — no independent S3 constructor coding.
- **P1:** baseline and possible native #3679 board evaluation; no publication, no mandate to implement. Source-native task lifecycle and network semantics remain in charge.
- **P2: NONE** — no speculative S3*, S4 or S5 expansion.

## 4. Illustrative native tests and rejection

These are **proposed cases, not executed** and do not constitute an implementation checklist to ship a controller now.

| Source-native scenario | Expected observable result | Reject |
| --- | --- | --- |
| Four-agent fixed pipeline, existing Task/Network baseline | Record exact invocations, tokens, terminal results and maintenance steps | No matched baseline |
| Optional board, task transition naming one next worker | Exactly the intended eligible agent receives the dispatch; others remain unwoken | Broad wake, duplicate effects or broken Task terminal |
| Stale owner/revision or unauthorized reassignment | No illegal dispatch; explicit denial result and unchanged task ownership | Caller silently overrides right or terminal state |
| If future S3 controller is justified, two lawful manager choices under identical snapshot | Different permitted downstream task allocations, both with returned actual Task results | Hardcoded scheduler owns the decisive decision, or receipt does not return |
| No S3 actor configured | Ordinary AG2 Task/Network behavior remains supported | Invented autonomous management behavior or default policy escalation |

Technical validation must be performed under AG2's then-current source-native pytest/ruff/mypy conventions and real public API, with failing behavior and exact commands recorded. No tests are claimed as executed by this plan.

## 5. Evidence ownership, falsification, alternatives and handoff

**Falsifiers for a separate S3 proposal:** current native means already meet the user goal; board does not lower unnecessary invocations; no independently necessary priority/capacity discretion; no lawful supported first-party actor/dispatch/feedback; or maintenance burden exceeds benefit. Any one is reason not to implement the S3 construction.

**Original-native alternative:** follow [#3679](https://github.com/ag2ai/ag2/issues/3679), preserve Task identity, use a small optional board and deterministic wake if a measured benefit exists. **Profile/Skills:** amend only from a source-backed semantic/procedure error. **Domain fork:** separately authorized experiment with exact boundary, no upstream adoption implication.

**Rights:** [Apache-2.0](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/LICENSE); [AI policy](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/.github/AI_POLICY.md) and contributor CLA apply to later PRs. Public fork Issue/PR and original maintainer interactions each require their own exact owner approval. **Cost: NOT_MEASURED**. **Decision: NO_GO / NO_USEFUL_CHANGE for S3 today**. Re-assess accepted >30-day-old Index grades before confident current-grade claims.
