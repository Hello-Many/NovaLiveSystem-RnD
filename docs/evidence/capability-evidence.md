# Capability evidence and funding case

**Updated November 9, 2026.**

NovaLiveSystem is an implemented biomimetic cognitive architecture and research platform for persistent,
human-centered cognitive work. SparkPlugged Technology Solutions is preparing a bounded Phase I research program
on a problem that becomes more important as AI systems retain context and learn across tasks: how can a system learn
from what actually happened without carrying a false lesson into the next context?

This page gives funders, research collaborators and commercial partners a concise view of the platform, the proposed
technical contribution and the work a Phase I award would support.

## The platform that exists today

| Platform capability | Implemented foundation | Why it matters to the research |
| --- | --- | --- |
| Persistent memory and continuity | RiverPulse, EchoMemory, conversation history and bounded context assembly preserve and select prior state. | The research concerns learning across interrupted, stateful work rather than isolated prompts. |
| Local inference and producer provenance | Dated runs used a local language engine and recorded whether the final response came from generation or fallback. | A learning system needs to distinguish the action it requested from the path that actually produced an outcome. |
| Cognitive routing and governed action | BridgeEngine coordinates specialized regions; planning and registered tools operate within authority boundaries. | Contracts and receipts can bind decisions, effective actions, overrides and terminal state. |
| Evidence infrastructure | Revision pins, native traces, state manifests, integrity checks and acceptance gates support reproducible review. | Phase I can measure attributable outcomes rather than relying on unverified self-report. |
| NovaCortex Operator Environment | The human-centered workspace lets a user direct work, inspect context, preserve constraints and recover continuity. | It provides a practical path from the research method to continuity software under user control. |

The private implementation, model weights, datasets, personal memory and raw operational logs are not part of this
public repository. The [architecture overview](../architecture/architecture-overview.md) describes the public system
topology, and the [runtime evidence guide](runtime-evidence-guide.md) explains how dated results are evaluated.

## The fundable technical question

When an AI controller proposes an action, the system may execute something different. A permission may be denied, a
memory source may be unavailable, a fallback may run, a retry may use new state, or a downstream component may
override the original choice. If the learner credits the proposal instead of the effective action, it can learn a
false lesson. If that lesson transfers to another task, the error can compound.

SparkPlugged proposes **receipt-grounded selective transfer (RGST)**:

`declared contract -> proposed action -> effective action -> execution receipt -> attributable outcome`

RGST separates three decisions:

1. **Execution learning** estimates what happens after an action is proposed, including execution, modification,
   denial, failure, cancellation and staleness.
2. **Attributable-outcome learning** updates utility only for the effective action supported by host-recorded evidence.
3. **Selective transfer** decides whether verified feedback may transfer to another task, must abstain, or must remain
   isolated.

The central research question is whether this separation can improve useful completion while reducing attribution
error and harmful cross-context transfer. The claim is intentionally falsifiable. RGST must be compared against
deterministic contract rules, no-sharing learning and equally informed generic transfer methods. If a simpler method
performs as well under the same information and cost constraints, the distinctive RGST hypothesis is not supported.

## What Phase I would establish

A six-month feasibility program would:

- build a reproducible benchmark of interrupted cognitive-work tasks with unavailable sources, stale state,
  fallbacks, overrides, retries and cancellation;
- implement RGST alongside strong baselines and ablations while holding the base model fixed;
- measure verified useful completion, attribution error, harmful transfer, abstention, evidence coverage and
  operating cost;
- test whether the method's benefit survives incomplete evidence and changes in task family;
- conduct bounded customer discovery around continuity difficulty, safeguards, current workarounds and willingness
  to pay; and
- produce an evidence-backed commercialization decision and a Phase II development path if the hypothesis survives.

The proposed feasibility study is nonclinical and does not require a claim that the research outcome is already
known. Funding would resolve the technical and commercial uncertainties under declared rejection conditions.

## Founder and company execution

SparkPlugged is led by founder and CTO **Ifejah “Spark” Greene**, a neurodivergent parent and caregiver who built
NovaLiveSystem from continuity problems she experienced across academic, technical and company work.

Greene learned through AI-assisted, mobile-first co-development. She began the first implemented NovaLiveSystem build
on two iPhones and an iPad and completed its first recorded model-training run on CPU within four months, before GPU
hardware was available. She architected and implemented the cognitive foundation and NovaCortex Operator Environment,
authored two registered preprints, brought the standalone continuity product EchoCopi to commercial release and then
into revision, submitted a receipted DOE Phase I pitch, and completed SAM.gov All Awards registration and CAGE
assignment.

That record establishes founder execution across research, productization and federal operations. It does not replace
external market discovery or prove RGST performance. The initial discovery hypothesis is a direct-user subscription
for neurodivergent adults doing complex academic or technical work across fragmented sessions; institutions are later
channels to test, not assumed buyers.

## Work with SparkPlugged

SparkPlugged is preparing for research funding, independent method review, target-user discovery and technical
collaboration in reliable persistent AI.

- **Research collaboration:** hello.many@sparkpluggedts.com
- **Funding, commercial and federal inquiries:** sparksupernova@sparkpluggedts.com
- **Company:** [sparkpluggedts.com](https://sparkpluggedts.com/)

Public material is governed by the repository [license](../../LICENSE). Private implementation access, licensing,
deliverables and diligence materials require a separate written agreement.

[Architecture](../architecture/architecture-overview.md) · [Research program](../research/research-status.md) ·
[Papers](../research/papers.md) · [Collaboration](../collaboration/support-and-collaboration.md)
