# The public R&D board

**Updated November 10, 2026.**

NovaLiveSystem's development runs in a private repository. Its progress is shown publicly on the
[NovaLiveSystem R&D board](https://github.com/users/SparkSupernova/projects/1), which lists items from **this**
repository. Each item is a stage or a piece of work described at the level of the [roadmap](roadmap.md) and the
[capability evidence](../evidence/capability-evidence.md): what it is for, what counts as done, and where the evidence
is or will be published. Source code, Nova's memory, datasets, model weights and raw logs are never part of a board item.

## How to read the board

| Column | Meaning |
| --- | --- |
| **Backlog** | Planned, not started. |
| **In progress** | Being built or being proven. |
| **In review** | Built; the evidence is under review before it is published. |
| **Done** | Published with its evidence, or implemented and recorded in the [changelog](changelog.md). |

**Priority** is read against the roadmap: **P0** is work the next published result depends on, **P1** is the next
stage of the program or evidence the funding decision needs, **P2** is planned work behind it. **Organ / System** names
the part of the architecture an item touches; **Lifecycle Stage** places it on the path from concept to validated,
documented capability.

## Board items

The items below are the board's public content. Titles and bodies match the board exactly; this page is their record.

### Platform foundation

- **Status:** Done · **Priority:** P1 · **Organ:** BridgeEngine · **Stage:** Implementation

Persistent memory and continuity, a local language engine with producer provenance, planning and governed tool use,
evidence infrastructure and the NovaCortex Operator Environment, implemented as one architecture. Evidence: the
[capability evidence](../evidence/capability-evidence.md) and the [roadmap](roadmap.md), platform foundation stage.

### Reply provenance and single-pass response

- **Status:** Done · **Priority:** P0 · **Organ:** BrocasArea · **Stage:** Validation & Drift

Every reply Nova returns records its producer, the local language engine or a stated fallback, together with a request
identifier shown beside the message in the app. One user turn produces one outward reply, and only the reply that was
returned enters Nova's memory. Landed November 10, 2026:
[changelog](changelog.md#november-10-2026---response-provenance-and-running-stack-diagnostics).

### Running-stack diagnostics

- **Status:** Done · **Priority:** P1 · **Organ:** Runtime & MCP · **Stage:** Implementation

An operator-only view of the running system: which regions are registered, whether the language engine is reachable,
the four channels of Nova's heartbeat with their freshness, and the producer of the last reply. It observes the running
system and never starts a second one. Landed November 10, 2026:
[changelog](changelog.md#november-10-2026---response-provenance-and-running-stack-diagnostics).

### Memory recall screening

- **Status:** In progress · **Priority:** P0 · **Organ:** BridgeEngine · **Stage:** Implementation

Strengthening the screening of memory brought forward into a conversation, while preserving historical records. The
first step, keeping past failure notices out of recalled memory, landed November 10, 2026
([changelog](changelog.md#november-10-2026---response-provenance-and-running-stack-diagnostics)). The next step extends
the same screening to earlier unlabelled records on every recall path. Completion evidence: the dated run below.

### Dated run through the app

- **Status:** In progress · **Priority:** P0 · **Organ:** BrocasArea · **Stage:** Validation & Drift

A question, a follow-up and a memory question asked through the app, with one selected reply per turn and the recorded
producer for each, released as a reviewed capture under the
[runtime evidence guide](../evidence/runtime-evidence-guide.md). Extends the dated provenance observations cited in
[what is built](../../README.md#what-is-built).

### Continuity across a restart

- **Status:** Backlog · **Priority:** P1 · **Organ:** BridgeEngine · **Stage:** Validation & Drift

Facts chosen before a restart are asked for after it, through the app, with the recall path recorded. A dated test of
the persistent memory and continuity claim in [what is built](../../README.md#what-is-built), released under the
[runtime evidence guide](../evidence/runtime-evidence-guide.md).

### Memory architecture reference

- **Status:** In progress · **Priority:** P1 · **Organ:** Docs & Sponsorship · **Stage:** Docs & Sponsorship

The public [conceptual architecture](../architecture/architecture-overview.md) is brought level with the implemented
memory system: how memories are written, how they are recalled, and what is eligible to come forward. Completion
evidence: the updated page and a changelog entry.

### Phase I readiness

- **Status:** In progress · **Priority:** P1 · **Organ:** Docs & Sponsorship · **Stage:** Architecture Spec

The RGST specification, rejection conditions, workplan, resource model and customer-discovery design, reviewed as a
research package, with a solicitation-specific submission decision. See the [roadmap](roadmap.md) and
[what funding would test](../../README.md#what-funding-would-test).

### Phase I feasibility

- **Status:** Backlog · **Priority:** P2 · **Organ:** Datasets & Probes · **Stage:** Validation & Drift

RGST, baselines and ablations on controlled interrupted-work fixtures, reported as reproducible results for useful
completion, attribution error, harmful transfer, abstention, coverage and cost. See
[what Phase I would establish](../evidence/capability-evidence.md#what-phase-i-would-establish).

### Interrupted-work benchmark

- **Status:** Backlog · **Priority:** P2 · **Organ:** Datasets & Probes · **Stage:** Concept & Intake

A reproducible benchmark of interrupted cognitive-work tasks with unavailable sources, stale state, fallbacks,
overrides, retries and cancellation: the first deliverable named under
[what Phase I would establish](../evidence/capability-evidence.md#what-phase-i-would-establish).

### Product discovery

- **Status:** Backlog · **Priority:** P1 · **Organ:** Docs & Sponsorship · **Stage:** Concept & Intake

Direct-user continuity needs, safeguards, current alternatives and willingness to pay, producing evidence-backed user,
payer and initial product requirements. P1 because the Phase II decision depends on it. See the [roadmap](roadmap.md).

### Phase II decision

- **Status:** Backlog · **Priority:** P2 · **Organ:** Docs & Sponsorship · **Stage:** Concept & Intake

Method performance, technical risk, product pull and delivery economics, ending in an advance, narrow, redirect or stop
decision with supporting evidence. See the [roadmap](roadmap.md).

## Disposition of the eight September cards

The board carried eight draft cards from September 2026. Their bodies name private repository paths, which the rule
above forbids, so every body is replaced regardless of disposition. Spark decides each row.

| September card | Covered by | Recommendation |
| --- | --- | --- |
| Tri-Heartbeat telemetry + PulseEngine health gating (Done) | Running-stack diagnostics; changelog December 2025 and November 2026 | Retire; the capability is recorded |
| EchoCopi continuity + public docs refresh (Done) | Changelog October and November 2026 | Retire; superseded by the published refresh |
| SparkPlugged Launch Package (Website, Releases, EchoCopi) (In progress) | Not covered | Keep as a thirteenth card, body rewritten without paths; Spark confirms status |
| Control Dataset Governance Overhaul (In progress) | Platform foundation, evidence infrastructure | Fold into one card, "Training-data governance", status confirmed by Spark |
| Stage 10 Probe & Holdout Alignment (In progress) | same | Fold into "Training-data governance" |
| Stage10 control dataset law + probe coverage (In progress) | same | Fold into "Training-data governance" |
| Stage 10 Dataset Release Log (Backlog) | same | Fold into "Training-data governance" |
| Stage11 probe manifest planning (Backlog, empty body) | Phase I feasibility | Retire |

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
> **Work with us:** research collaboration, <hello.many@sparkpluggedts.com>; funding, commercial and federal inquiries,
> <sparksupernova@sparkpluggedts.com>; [sparkpluggedts.com](https://sparkpluggedts.com/).
>
> The source code, Nova's private memory, datasets, model weights and raw logs stay private.
