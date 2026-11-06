---
layout: home
title: Home
nav_order: 1
description: "Extraction Loop & Stash Kit is the complete extraction loop for Unity 6: a Tetris-grid stash, one raid state machine, itemized settlement, insurance, traders, and saving that survives death — plugged into the controller you already use."
permalink: /
---

# Extraction Loop & Stash Kit
{: .fs-9 }

The complete extraction loop for Unity: **stash, raid, extract, insurance and traders** — ready to plug into the controller you already use.
{: .fs-6 .fw-300 }

[Get started]({{ site.baseurl }}/docs/getting-started/){: .btn .btn-primary .fs-5 .mb-4 .mb-md-0 .mr-2 }
[Buy on the Unity Asset Store](https://assetstore.unity.com/publishers/118262){: .btn .fs-5 .mb-4 .mb-md-0 }

---

## See the loop run

![Extraction Loop & Stash Kit]({{ site.baseurl }}/assets/images/cover.jpg)

The whole loop in one pass — stash, insure, deploy, loot, extract, settle:

![The extraction loop, animated]({{ site.baseurl }}/assets/images/extraction-loop.gif)

<video controls preload="metadata" style="max-width:100%" src="{{ site.baseurl }}/assets/video/extraction-loop-demo.mp4"></video>

![The stash after a successful raid]({{ site.baseurl }}/assets/images/showcase-stash-grown.jpg)
*The stash, grown: 1,431 Credits and five stacks after one clean extraction.*

![Inside the Greyline Depot reference raid]({{ site.baseurl }}/assets/images/showcase-in-raid.jpg)
*Inside Greyline Depot, the playable greybox reference raid.*

![Settlement after a death]({{ site.baseurl }}/assets/images/showcase-death-ledger.jpg)
*Death has a ledger: the insured rifle comes back; the uninsured medkit does not.*

## Everything around the shooting

You already have movement and shooting solved. What an extraction game still needs is everything around the shooting: the stash your gear lives in, the raid that puts it at risk, the settlement that decides what you kept and what you lost, the insurance that brings a favourite weapon back, the trader who turns salvage into currency, and the save file that has to hold all of it without ever corrupting. This kit is that layer, as one coherent package built around a single state machine — not four assets glued together.

- **A Tetris-grid stash** — items occupy real shapes on the grid, rotate in 90-degree steps, and stack where their data says they stack. Placement is validated, and a rejected placement changes nothing and says why in plain words.
- **One raid state machine** — every raid moves InStash, Deploying, InRaid, then Extracted or Died, then Settlement. Illegal transitions are rejected and logged; extraction and death enter through the same integration calls your controller code makes.
- **Settlement you can read** — an itemized record: kept, lost, insured and on its way back, sold, and fees. Deterministic: the same inputs always produce the same record, which makes your economy auditable.
- **Insurance that keeps its word** — insure gear at deploy time; die, and insured items are scheduled for return and tracked in a pending-returns list until they land back in your stash — exactly once, never duplicated, never vanished.
- **Traders with atomic transactions** — buy and sell run quote, then confirm: funds and items move together or not at all. Trader stock, prices and margins are data assets, not code.
- **Saving that survives the worst day** — one versioned JSON document with atomic write, a last-good backup, recovery that loads the backup and says so, and a schema migration chain.

## See it work in ten minutes

The **Reference Raid** ships in the package: a solo playable scene, Greyline Depot. Choose the starter rifle and medkit on the Stash Board, insure the rifle, deploy, loot the two salvage crates, extract — and watch the settlement add your loot to a stash that visibly grew. Then run it again, die on purpose, and watch the insured rifle come back. See [Reference Raid — Greyline Depot]({{ site.baseurl }}/docs/reference-raid/).

## Plugs into your controller

The kit ships no character controller and never will: it integrates through a **documented API** (BeginDeploy, RegisterLoot, TriggerExtraction, RegisterDeath) and the included **generic adapter**, which passes the kit's adapter conformance suite. The core is netcode-agnostic and compiles in a bare project with no controller and no transport package present. See [Integration API]({{ site.baseurl }}/docs/integration-api/).

## The honest frame

Version 1 is a **solo loop with transport hooks** — no multiplayer session, no matchmaking, no relay or server ships, and third-party controller adapters are **not** a verified v1 feature. The full list is [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).

> Automated verification for v1.0.0: **57/57** EditMode tests and **2/2** PlayMode tests green on Unity 6000.5.4f1, including a 100-raid economy-integrity simulation; bare-project compile verified, and the Reference Raid is playable solo and PlayMode-proven end to end. **Unity 6 only** — v1 does not support Unity 2022.3.
