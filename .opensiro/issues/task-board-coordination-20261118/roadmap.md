# AG2 capability roadmap receipt — 2026-11-18

## Identity and pins

- Original repository: ag2ai/ag2
- Original HEAD: f3943efb5546c4dbaecaf08706eb2bc16e56c602
- Observed at: 2026-11-18
- Accepted Index assessment: https://github.com/opensiro/vsm-harness-index/blob/34e11ec4dd52e1ba3ee0111d8bca73f13918f54f/assessments/ag/ag2.md
- Accepted assessment blob SHA: cc442691abb833236f48f30206580bb17c258f5c
- Accepted review ref: 3211bb19832049e7abe1a5742b6d177274bff723
- Accepted reviewed at: 2026-09-18
- System in focus: AG2 first-party Agent plus optional Network Hub/Agent organization; AG2 Classic excluded
- Index main commit: 34e11ec4dd52e1ba3ee0111d8bca73f13918f54f
- Accepted Profile version: 0.2.2
- Accepted Methodology version: 0.3.1
- Accepted Index catalog row: 110 | ag2 | https://github.com/ag2ai/ag2 | 3211bb19832049e7abe1a5742b6d177274bff723
- Fork: https://github.com/opensiro-contributions/ag2 (verified fork of ag2ai/ag2)
- Fork default head at capture: e1a63487a9b11890fc1801e1ff87a06bf63e0475 (separate from current original HEAD)
- Last accepted successful assessment date: 2026-09-18 (61 calendar days earlier); no later successful semantic reassessment established for this case
- Human Issue: [issue.md](issue.md)
- AI/developer constructor contract: [constructor-sufficiency.md](constructor-sufficiency.md)
- Decision: NO_GO — no separate S3 constructor now

## Rights and authority

- Original license: Apache-2.0, source [LICENSE](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/LICENSE).
- Original [AI policy](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/.github/AI_POLICY.md) permits reviewed AI assistance, requires accountable claims and contributor CLA certification for a submitted PR; personal CLA signature is not assumed.
- Verified working fork: opensiro-contributions/ag2, parent exactly ag2ai/ag2, separate metadata branch initialized from pinned fork default HEAD; owner control initialized PAUSE, attention DORMANT with no inferred RESUME/ALLOW.
- Plan-only metadata capture is not product-code implementation or public GitHub Issue/PR approval.

## Existing work / overlap

- [AG2 #3679](https://github.com/ag2ai/ag2/issues/3679): OPEN first-party request for shared board and waking only `next`; reuse this rather than duplicate.
- [Task lifecycle source](https://github.com/ag2ai/ag2/blob/f3943efb5546c4dbaecaf08706eb2bc16e56c602/ag2/task.py): SHIPPED agent-owned Task events/checkpoints, explicitly no framework scheduling.
- [PR #3576](https://github.com/ag2ai/ag2/pull/3576): MERGED on 2026-11-03, unified agent/delegation Task lifecycle.
- [PR #2775](https://github.com/ag2ai/ag2/pull/2775): MERGED, Network protocols and control surfaces.
- [PR #3466](https://github.com/ag2ai/ag2/pull/3466): OPEN per-batch concurrent tool cap, a different task-local concern; not a shipped board or S3 actor.
- No source-verified accepted shared-board implementation identified in bounded issue/PR/source checks; this is not proof of global absence.

## Function ownership

- Historical accepted vector: S1=A; S2=C; S3=—; S3*=—; S4=—; S5=—.
- S1 agent owns actual tool work. S2 Network discussion first-party coordination already supports C; no mandatory second S2 constructor.
- Current original Task/Hub event/state surfaces do not establish a developer-composable S3 actor with whole-system discretionary current commitments/capacity decisions and returned effect; static `next` task routing is not such an actor.
- Historical grade freshness: 61 days; recommend an Index-owned re-assessment for any new current-HEAD VSM ownership claim, not a new published grade by roadmap.

## Capability priority

- P0: NOT ADMITTED — no useful independent whole-system S3 C target is supported yet, thus no speculative constructor implementation.
- P1: original-native #3679 benchmark of fixed four-agent Task/Network baseline against optional single-next TaskBoard, preserving correct final outcomes and authorization, if separately selected.
- P2: NONE — no optional S3*/S4/S5/parent-mode target without evidence.
- Conditional S3 C sufficiency: current-work snapshot + lawful intervention options + developer-composed autonomous controller + enforced Task/Network dispatch + actual feedback into subsequent control; none of these proposed additions is claimed shipped. See [AI contract](constructor-sufficiency.md).

## Implementation options

- Primary NO_GO: do not build a parallel VSM-labelled S3 service, fork-local code patch or competing original Issue solely because accepted S3 was —.
- Source-native alternative: track existing [#3679](https://github.com/ag2ai/ag2/issues/3679); a real improvement would require one-next wake, proper Task terminals, safe concurrency/ownership and matched invocation/token savings. This is a future scoped implementation choice, not an OpenSiro permission to start.
- A later material S3 need would require a real organization-level decision actor and first-party feedback loop, with positive, different-lawful-choice, unauthorized/stale-state and baseline acceptance evidence.

## Specification and domain alternatives

- Profile/Skills feedback only if evidenced function-first interpretation fails, not to manufacture C.
- An authorized domain-specific fork could separately test a manager-controlled task board with explicit cost comparison and boundary, with no promise of third-party maintainer adoption.

## Cost experiment

- Compare equivalent four-agent pipelines with same tasks/tools/stop conditions and actual correct output: current Task+Network baseline versus optional single-next board.
- Measure agent wake-ups, off-target deliveries, input/output tokens, implementation/integration/review/test effort and later maintenance effort.
- Cost status: NOT_MEASURED
- No cost saving or new grade is claimed.

## Delivery and publication

- Result: NO_USEFUL_CHANGE
- Decision: NO_GO for a separate OpenSiro/VSM S3=C feature now; source-native #3679 remains a valid independent feature request.
- Work mode: PLAN_ONLY; original HEAD/current code inspected, no AG2 code/tests modified or run.
- Public fork GitHub Issue: NOT PUBLISHED; exact current-conversation owner approval required for the complete Human title/body.
- External issue: DRAFT — NOT PUBLISHED
- No external original Issue/PR/comment or public fork-local PR created.
- Next decisive action: no autonomous continuation; record the NO_GO and, upon a separately directed task, review source-native #3679 benchmark/maintainer response or conduct a pinned Index re-assessment.
