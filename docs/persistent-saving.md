---
layout: default
title: Persistent Saving
nav_order: 12
description: "The whole loop persists as one versioned JSON document — stash, currency, pending returns, trader deltas, statistics — with atomic write, last-good backup recovery, and a schema migration chain."
---

# Persistent Saving
{: .no_toc }

The loop's whole state persists as **one versioned JSON save document**:

- the **stash**,
- **currency**,
- **pending returns** (insured items on their way back),
- **trader deltas**,
- **statistics**.

One document means one consistency story: the stash a settlement wrote is the stash the next raid reads, and insurance pending in the document is insurance that survives a restart.

## Atomic write, honest recovery

- Writes are **atomic (write-temp-and-swap)**: an interrupted write cannot leave a half-written document.
- A **backup of the last good document** is kept. On a corrupted save, recovery **loads the backup and says so** — a corrupted save never presents as a silently emptied stash.
- The document carries a **schema version with a migration chain**, so when the kit's save format evolves, older documents migrate forward through registered steps instead of failing to load.

Saving is exercised by the same loop the tests drive: the 100-raid economy-integrity simulation persists and reloads through this document (see [Settlement]({{ site.baseurl }}/docs/settlement/)).
