# AG2 — independent S3 construction sufficiency and native counterfactual (AI)

**PLAN_ONLY · proposal-stage NO_GO · research NO_USEFUL_CHANGE · NOT IMPLEMENTED / NOT PUBLISHED**

**Target transition:** NO_QUALIFIED_C_TARGET
**Proposal-stage decision:** NO_GO
**Research disposition:** NO_USEFUL_CHANGE

[issue.md](issue.md) · [roadmap.md](roadmap.md).

## Function-specific six-function screen

System in focus: first-party AG2 Agent and optional Network Hub at original 6d2dd8bab8af873ea29ed759cfacb572466d925e, not AG2 Classic, tenant applications or downstream schedulers. Historical six-function state and associated exclusion explanations are in the Human table and [roadmap.md](roadmap.md). S1 model/tool actor already autonomously executes work; S2 discussion protocol is a function-specific coordination C. S3 candidate would require organizational current-work discretion, not a fixed routing rule. S3* listener, S4 future analysis and S5 identity cannot be counted from Task lifecycle, telemetry or human parent authority.

## Track A: actual source, Issue/PR and source-native baseline

- Shipped first-party [Task](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/ag2/task.py) emits started/progress/completed/failed/cancelled and checkpoints; scheduling belongs to calling agent/application.
- [Network TaskMirror]( https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/website/docs/user-guide/network/task_observation.mdx ) returns Task activity; [AgentClient targeted envelopes](https://github.com/ag2ai/ag2/blob/6d2dd8bab8af873ea29ed759cfacb572466d925e/website/docs/user-guide/network/agent_clients.mdx) already expose owner-scoped sends and callbacks.
- [Original #3679](https://github.com/ag2ai/ag2/issues/3679) OPEN requests task board, status, next-only wake, scoped inbox and four-agent comparison. This is the exact owner-native feature, NOT shipped.
- [#3576](https://github.com/ag2ai/ag2/pull/3576) MERGED Task lifecycle, [#2775](https://github.com/ag2ai/ag2/pull/2775) MERGED Network protocols, [#3128](https://github.com/ag2ai/ag2/pull/3128) MERGED middleware. [#3466](https://github.com/ag2ai/ag2/pull/3466) OPEN @81aef1444d0e55ae242591b6b4fae2e43b294599 is per-tool concurrency and not shared agent assignment.
- Cheapest current native comparator: application-owned targeted AgentClient / single-next host logic using existing Task returns. No source-supported claim it is always cheaper or sufficient; experiment NOT_RUN.

## Track B: on-top options independently compared in original 2026-11-19 study

| Candidate | Exact on-top source interface | Claimed incremental difference | Why no separate C target now |
| --- | --- | --- | --- |
| Reuse existing host | Existing targeted Network sends, Task events | Avoid broad room wake without code patch | No new first-party decision actor, but solves simplest task |
| Integrate original #3679 | Optional TaskBoard next/status inbox + Task terminal linkage | Durable shared source-of-truth and strict one-next wake | #3679 already owns this user outcome; no OpenSiro-specific separate delta |
| Adjacent cross-process retry adapter | Conditional versioned/idempotent next activation and TaskMirror receipts | Avoid duplicate/lost wake after crash/retry | No observed residual incident, no demonstrated new parent authority/return need |
| Autonomous S3 actor | Parent-capped whole-current task/capacity snapshot, options, composed managerial choice, daemon/Hub-side dispatch, feedback | Current priority/commitment decision beyond next-only static scheduling | Not established as an operator request or as distinct from original owner's task board/host |

## P0 / P1 / P2 and falsifiable tests

**P0 NO_QUALIFIED_C_TARGET / NO_GO.** Do not write a duplicate VSM management service or release another Issue about #3679. **P1** is owner-led original #3679 benchmark and possible native adaptation, not a current OpenSiro feature authorization. **P2 NONE.**

**Positive benchmark (NOT_RUN):** four-agent research, write, review, integrate under identical tools/inputs: host selective routing, proposed original TaskBoard, then any candidate adapter only if baseline fails. Count exact agent wakeups, unaffected watcher silence, proper terminal Task outcomes, invocation/token/latency totals and maintenance effort.

**Negative (NOT_RUN):** unauthorized writer, stale status revision, crash/retry, duplicate events or cancellation must not produce extra invocation or cross-principal access.

**S3 constructor gate:** if an independent actor is ever proposed, require two distinct lawful whole-current capacity choices that alter later actual AG2 work under a genuine first-party authority and return. Without that, the feature is S2/transport/Task bookkeeping, not S3=C.

**Falsifier:** host targeted route or native #3679 meets selective-wake objective with correct task status at lower/equal integration/operation cost; then separate S3 C lacks a material target. Reopen only on a reproducible materially unmatched current-management problem and proof of source-native rights.

## Historical provenance and permission

The original read-only outcome was reported in [Upstream #58 dated comment](https://github.com/opensiro/upstream/issues/58#issuecomment-7012239664) with 2026-11-19 original 6d2dd8bab8af873ea29ed759cfacb572466d925e; it had PAUSE/DORMANT at that time and did not edit fork metadata. The previous 2026-11-18 [AG2 case](https://github.com/opensiro-contributions/ag2/blob/3c4d4ba7f3322670cc8c905f1ccaf9cd31a2eb40/.opensiro/issues/task-board-coordination-20261118/roadmap.md) remains in Git history. Current fork ACTIVE/ALLOW is new owner attribution; this sync records the same independent NO_GO but does NOT assert fresh v0.18 independent reasoning or test execution.

Original Apache-2.0/AI policy and CLA certification apply to any actual external PR. No native test, product source edit, approved public Issue/PR, external original communication, new Index grade or cost result.
