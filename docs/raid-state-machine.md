---
layout: default
title: Raid State Machine
nav_order: 8
description: "One legal path for every raid: InStash, Deploying, InRaid, Extracted, Died, Settlement. Illegal transitions are rejected and logged, and each raid produces an itemized raid record."
---

# Raid State Machine
{: .no_toc }

Every raid in the kit moves through **one state machine** — the same machine in the Reference Raid, in the test suite, and in your game, because all three drive it through the same calls.

## The states

**InStash → Deploying → InRaid → Extracted / Died → Settlement**

- **InStash** — gear is in the stash; nothing is at risk.
- **Deploying** — the loadout is committed; insurance bought here takes effect (see [Insurance]({{ site.baseurl }}/docs/insurance/)).
- **InRaid** — the raid is live; loot is registered as it is picked up.
- **Extracted** — the raid ended in extraction: loot is kept.
- **Died** — the raid ended in death: the lose-on-death rules apply.
- **Settlement** — the raid closes with an itemized record (see [Settlement]({{ site.baseurl }}/docs/settlement/)).

## One legal path

Transitions outside that path are **illegal — rejected and logged**, never silently forced. A raid cannot settle before it ends, cannot extract after it died, cannot deploy twice. The log of a rejected transition names what was attempted, so an integration bug shows up as a readable record instead of corrupted state.

## The raid record

Each raid produces an **itemized raid record** — what was carried in, what was looted, how it ended. Settlement is a deterministic function of that record, the stash, and your economy config; the record is what makes the outcome auditable.
