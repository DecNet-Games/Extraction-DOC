---
layout: default
title: What v1 Is Not
nav_order: 17
description: "Extraction Loop & Stash Kit v1's explicit boundaries: no multiplayer, session, or matchmaking; third-party controller adapters not verified; not a controller, weapon system, camera rig, or complete game; not an anti-cheat system."
---

# What v1 Is Not
{: .no_toc }

This page is the honest list. Everything the kit v1 does is documented in these pages; everything here is what it deliberately does not do.

## No multiplayer in v1

Version 1 is a **solo loop with transport hooks**. It includes **no multiplayer session, no matchmaking, no relay or server, and no hosted service of any kind**. The hooks assembly exposes raid-state replication payloads for **your own** transport code — and the kit makes no promise about that code. If you read any page here as "multiplayer included", that reading is wrong; see [Transport Hooks]({{ site.baseurl }}/docs/transport-hooks/).

## Third-party controller adapters are not verified

v1 ships the **generic adapter** and the **documented API**, and the generic adapter passes the kit's conformance suite. Controller-specific bridge components in the package are **unverified starting points, not supported adapters** — conformance for any specific third-party controller is unproven and is not claimed anywhere in this documentation.

## Not a controller, weapon system, or game

The kit is **not a character controller, weapon system, camera rig, or a complete game** — and never will be the controller part. The Reference Raid is a labelled demonstration of the loop; sample items, prices and balance are sample content.

## Not an anti-cheat system

Settlement is **deterministic and auditable**; the kit is **not an anti-cheat or server-authority system**. It makes your single-player (or your own authority model's) economy consistent and provable — it does not police clients.

## Unity 6 only

v1 supports **Unity 6 only** (6000.0 LTS and later 6.x), verified on Unity 6000.5.4f1. **Unity 2022.3 is not supported** in v1.
