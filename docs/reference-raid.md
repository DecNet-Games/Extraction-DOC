---
layout: default
title: Reference Raid — Greyline Depot
nav_order: 15
description: "The shipped solo playable sample scene: stash, deploy, loot, extract, settlement, trader — the full loop, labelled as the demonstration it is."
---

# Reference Raid — Greyline Depot
{: .no_toc }

The Reference Raid is the kit's shipped demonstration: a **solo playable sample scene** that runs the full loop end to end. Open it from the Home window's **Samples & Scenes** section.

## The run

1. **Stash** — on the Stash Board, choose the **starter rifle and medkit**.
2. **Insure** — insure the rifle at deploy time (shipped default fee: 15 percent).
3. **Deploy** — the state machine moves InStash → Deploying → InRaid.
4. **Loot** — pick up the **two salvage crates**.
5. **Extract** — settlement produces the itemized record, and your loot lands in a stash that visibly grew.
6. **Trade** — the **Depot Trader** turns salvage into currency through quote-then-confirm.
7. **Run it again and die on purpose** — the uninsured gear is lost, line by line; the insured rifle enters the pending-returns list and comes back, exactly once.

## What the scene is — and is not

The Reference Raid is a **labelled demonstration of the loop**, PlayMode-proven end to end in the verified record. It is not a complete game: sample items, prices and balance are sample content, and the scene ships no controller beyond what the loop demonstration needs. Your game brings its own controller and calls the same [integration API]({{ site.baseurl }}/docs/integration-api/) the demo's flow runs on.
