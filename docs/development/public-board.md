# The public R&D board

**Updated November 10, 2026.**

NovaLiveSystem's development runs in a private repository. Its progress is shown publicly on the
[NovaLiveSystem R&D board](https://github.com/users/SparkSupernova/projects/1), which lists items from **this**
repository. Each item here is a stage or a piece of work described at the level of the [roadmap](roadmap.md) and the
[capability evidence](../evidence/capability-evidence.md): what it is for, what counts as done, and where the evidence
will be published. Source code, Nova's memory, datasets, model weights and raw logs are never part of a board item.

## How to read the board

| Column | Meaning |
| --- | --- |
| **Backlog** | Planned, not started. |
| **In progress** | Being built or being proven. |
| **In review** | Built; the evidence is under review before it is published. |
| **Done** | Published with its evidence, or implemented and recorded in the [changelog](changelog.md). |

**Priority** is read against the roadmap: **P0** is the work the next published result depends on, **P1** is the next
stage of the program, **P2** is planned work behind it. **Organ / System** names the part of the architecture an item
touches; **Lifecycle Stage** places it on the path from concept to validated, documented capability.

## Board items

The items below are the board's public content. Titles and bodies match the board exactly; this page is their record.

### Platform foundation

- **Status:** Done · **Priority:** P1 · **Organ:** BridgeEngine · **Stage:** Implementation

Persistent memory, bounded context, cognitive routing, local inference, governed action and evidence infrastructure,
implemented as one architecture. Completion evidence: the implemented architecture and dated provenance observations
recorded in the [capability evidence](../evidence/capability-evidence.md).

### Reply provenance and single-pass response

- **Status:** Done · **Priority:** P0 · **Organ:** BrocasArea · **Stage:** Validation & Drift

Every reply Nova returns now records where it came from, the local language engine or a stated fallback, together with
a request identifier that the app shows beside the message. One user turn produces one outward reply; only the reply
that was actually returned becomes part of Nova's memory. Landed November 10, 2026.

### Running-stack diagnostics

- **Status:** Done · **Priority:** P1 · **Organ:** Runtime & MCP · **Stage:** Implementation

An operator-only view of the running system: which regions are registered, whether the language engine is reachable,
the four channels of Nova's heartbeat with their freshness, and the source of the last reply. It observes the running
system and never starts a second one. Landed November 10, 2026.

### Memory recall screening

- **Status:** In progress · **Priority:** P0 · **Organ:** BridgeEngine · **Stage:** Implementation

Memory that is brought forward into a conversation is screened for eligibility before it reaches the language engine,
so that a past failed generation can never be recalled as if it were Nova's own words. Historical records are kept
intact; only what is eligible to be fed back changes. Completion evidence: the live demonstration below.

### Live demonstration through the app

- **Status:** In progress · **Priority:** P0 · **Organ:** BrocasArea · **Stage:** Validation & Drift

A question, a follow-up and a memory question asked through the app, with one selected reply per turn and the recorded
source for each. The first of the results promised under "What we're proving next". Published here with its evidence
after review.

### Recall of chosen facts across a restart

- **Status:** Backlog · **Priority:** P1 · **Organ:** BridgeEngine · **Stage:** Validation & Drift

Facts chosen before a restart are asked for after it, through the app, with the recall path recorded. The second result
promised under "What we're proving next".

### Memory architecture reference

- **Status:** In progress · **Priority:** P1 · **Organ:** Docs & Sponsorship · **Stage:** Docs & Sponsorship

The public [conceptual architecture](../architecture/architecture-overview.md) is brought level with the implemented
memory system: how memories are written, how they are recalled, and what is eligible to come forward. Completion
evidence: the updated page and a changelog entry.

### Phase I readiness

- **Status:** In progress · **Priority:** P1 · **Organ:** Docs & Sponsorship · **Stage:** Architecture Spec

The RGST specification, rejection conditions, workplan, resource model and customer-discovery design, reviewed as a
research package, with a solicitation-specific submission decision. See the [roadmap](roadmap.md).

### Phase I feasibility

- **Status:** Backlog · **Priority:** P2 · **Organ:** Datasets & Probes · **Stage:** Validation & Drift

RGST, baselines and ablations on controlled interrupted-work fixtures, reported as reproducible results for useful
completion, attribution error, harmful transfer, abstention, coverage and cost.

### Interrupted-work recovery study

- **Status:** Backlog · **Priority:** P2 · **Organ:** Datasets & Probes · **Stage:** Concept & Intake

A planned application study of recovery after interruption in scientific work, the first applied setting named under
"What we're proving next".

### Product discovery

- **Status:** Backlog · **Priority:** P2 · **Organ:** Docs & Sponsorship · **Stage:** Concept & Intake

Direct-user continuity needs, safeguards, current alternatives and willingness to pay, producing evidence-backed user,
payer and initial product requirements.

### Phase II decision

- **Status:** Backlog · **Priority:** P2 · **Organ:** Docs & Sponsorship · **Stage:** Concept & Intake

Method performance, technical risk, product pull and delivery economics, ending in an advance, narrow, redirect or stop
decision with supporting evidence.

## What never appears on the board

Source file paths, private memory contents, dataset and model artefacts, raw logs, internal planning records, and
defect inventories. Problems found during development are repaired in the private repository and appear here only as
the capability they produced, once it is proven.

## Project description

The board's own description page reads:

> **NovaLiveSystem** is a biomimetic cognitive architecture by SparkPlugged Technology Solutions: AI approached as a
> developing mind, not a tool. This board shows the public shape of its research and development: what is built,
> what is being proven, and what comes next. Each item links to its evidence when the evidence is published.
>
> **Start here:** [NovaLiveSystem R&D](https://github.com/Hello-Many/NovaLiveSystem-RnD) · [Roadmap](https://github.com/Hello-Many/NovaLiveSystem-RnD/blob/main/docs/development/roadmap.md) · [Capability evidence](https://github.com/Hello-Many/NovaLiveSystem-RnD/blob/main/docs/evidence/capability-evidence.md)
>
> **Work with us:** research collaboration, hello.many@sparkpluggedts.com; funding, commercial and federal inquiries,
> sparksupernova@sparkpluggedts.com; [sparkpluggedts.com](https://sparkpluggedts.com/).
>
> The source code, Nova's private memory, datasets, model weights and raw logs stay private.
