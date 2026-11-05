---
layout: default
title: FAQ
nav_order: 18
description: "Straight answers: Unity 6 only, what controller support actually means, whether multiplayer is included (it is not), how insurance returns work, and what happens to a corrupted save."
---

# FAQ
{: .no_toc }

## Which Unity versions are supported?

**Unity 6 only** (6000.0 LTS and later 6.x), verified on Unity 6000.5.4f1. **v1 does not support Unity 2022.3.**

## Does it work with my character controller?

The kit integrates through a **documented API** (BeginDeploy, RegisterLoot, TriggerExtraction, RegisterDeath) and an included **generic adapter**, which passes the kit's adapter conformance suite. Controller-specific adapters are **not** a verified v1 feature — bridge components in the package are unverified starting points. See [Integration API]({{ site.baseurl }}/docs/integration-api/).

## Is multiplayer included?

**No.** v1 is a solo loop with **transport hooks**: a hooks assembly exposes raid-state replication payloads for your own transport code. No session, matchmaking, relay, server, or hosted service ships. See [Transport Hooks]({{ site.baseurl }}/docs/transport-hooks/).

## How does insurance return my item?

Insure at deploy time (shipped default: 15 percent fee, return after one raid cycle). On death the item is scheduled for return and tracked in the **pending-returns list** until it lands back in your stash — **exactly once**, never duplicated, never vanished. See [Insurance]({{ site.baseurl }}/docs/insurance/).

## Can a settlement be wrong without anyone noticing?

Settlement is **deterministic** — same raid record, stash, and economy config, same itemized record — and every movement has a line: kept, lost, insured-pending, sold, fees. See [Settlement]({{ site.baseurl }}/docs/settlement/).

## What happens if the save file corrupts?

The loop state is one versioned JSON document with atomic writes and a **last-good backup**. Recovery loads the backup **and says so** — a corrupted save never presents as a silently emptied stash. See [Persistent Saving]({{ site.baseurl }}/docs/persistent-saving/).

## Does the kit need a networking package to install?

No. The core is netcode-agnostic and is verified compiling in a **bare project with no controller and no transport package present**.
