---
layout: default
title: Integration API
nav_order: 13
description: "The kit ships no controller: it integrates through a documented API — BeginDeploy, RegisterLoot, TriggerExtraction, RegisterDeath — and the included generic adapter, which passes the kit's adapter conformance suite."
---

# Integration API
{: .no_toc }

The kit ships **no character controller and never will**. Your controller keeps doing movement and shooting; the kit wraps the loop around it through a documented integration surface. Extraction and death enter through the **same integration calls your controller code makes** — so the loop in your game is the loop that was tested.

## The core calls

- **BeginDeploy** — commit the loadout and enter the raid path (insurance bought at deploy takes effect here).
- **RegisterLoot** — register looted items with the live raid.
- **TriggerExtraction** — end the raid in extraction.
- **RegisterDeath** — end the raid in death.

Each call drives the [raid state machine]({{ site.baseurl }}/docs/raid-state-machine/): a call that is illegal in the current state is **rejected and logged**, not forced.

## The generic adapter

The kit ships a **generic adapter** for wiring the loop to the controller you already use, and the adapter **passes the kit's adapter conformance suite** — that suite result is the integration claim v1 makes.

## What is not claimed

**Third-party controller adapters are not a verified v1 feature.** Controller-specific bridge components in the package are **unverified starting points, not supported adapters**. v1's supported integration surface is the generic adapter and the documented API — anything controller-specific is yours to verify against the conformance suite. See [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
