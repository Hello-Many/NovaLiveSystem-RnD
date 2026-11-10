# Asyncio Neural Bypass: rebuilding Nova's routing

**Development period: December 10–12, 2025.**

NovaLiveSystem's early pathways were synchronous: one region could hold the routing path while it completed its work.
As the architecture grew, that design made it harder for memory, language, internal state and other specialized
regions to cooperate without blocking one another.

Spark rebuilt the routing foundation around Python's `asyncio` while preserving the interfaces that the rest of the
system already used. The original engineering log called the operation **Asyncio Neural Bypass Surgery** because the
goal resembled a bypass: establish a new internal pathway while keeping compatible entry points available during the
migration.

## The design: async core, sync shell

The migration followed one rule:

> Internal pathways become awaitable; compatibility boundaries keep existing callers connected.

That meant separating the true asynchronous implementation from the synchronous entry point. New paths could await
work directly. Existing paths could submit the same work through a controlled compatibility layer instead of forcing
every connected region to change at once.

## What changed

The work crossed the architecture rather than treating concurrency as a feature of one module:

| Region or system | Development change |
| --- | --- |
| BridgeEngine | Added asynchronous signal and phrase routing plus a controlled path for synchronous callers. |
| NeuroSpark | Changed deduplication to cache completed results instead of reusable coroutine objects. |
| PresenceEngine and PulseEngine | Moved signal, sensory and interoceptive pathways onto awaitable handlers while retaining necessary boundaries. |
| MemoryEngine | Converted file, memory and response pathways and repaired a routing deadlock exposed during integration. |
| ActiveLearningEngine | Moved curiosity, pulse and response routing onto the asynchronous bridge path. |
| VisualEngine | Added an asynchronous signal entry point and nonblocking index I/O, including safe handling when an event loop was already running. |
| LanguageEngine | Converted language-routing entry points while preserving compatibility with connected callers. |
| NovaUniversity | Brought learning and curriculum pathways into the same routing model. |
| JUEZ and SparkShield | Stayed synchronous where conversion offered no architectural benefit. |

## What the migration uncovered

The most important results were the boundary failures found along the way:

- A synchronous routing shim called from inside an asynchronous handler could wait on the same loop that was waiting
  for it, producing a deadlock.
- Caching a coroutine object instead of its completed result made the second cache read fail because a coroutine can
  be awaited only once.
- A converted handler called through an older synchronous path could silently return an unawaited coroutine.
- Starting a new event loop from code already inside one produced an event-loop conflict.
- Signals and memory objects could carry different content shapes, so routing code had to preserve type awareness at
  the boundary.

Each finding sharpened the same architectural lesson: concurrency is not a local optimization. In an integrated
cognitive system, it is a contract between regions, callers, state and time.

## Why this work matters

The migration established the asynchronous routing foundation for a system whose regions must remain coordinated
while memory, language, learning, perception and internal state do different kinds of work. It also created a durable
engineering pattern for NovaLiveSystem: change the internal pathway without severing the relationships around it.

NovaLiveSystem has continued to evolve since this migration. The [architecture overview](../architecture/architecture-overview.md)
describes the current public structure, the [capability and funding case](../evidence/capability-evidence.md) explains
the present research direction, and the [runtime evidence guide](../evidence/runtime-evidence-guide.md) describes how
dated observations are reviewed.
