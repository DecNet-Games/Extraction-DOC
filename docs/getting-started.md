---
layout: default
title: Getting Started
nav_order: 2
description: "From the Asset Store download to a completed raid: install the kit, run the one-click setup, and play the Reference Raid end to end."
---

# Getting Started
{: .no_toc }

The kit works in one Editor window and one loop: **stash** your gear, **deploy** into a raid, **loot**, **extract** (or die), and **settle** — with insurance and traders wrapped around the same state machine. This section takes you from the Asset Store download to a completed raid.

## The path

1. [Install]({{ site.baseurl }}/docs/installation/) the package from the Unity Asset Store.
2. Follow the [Quick Start]({{ site.baseurl }}/docs/quick-start/): open the Home window, run the one-click setup, and play the Reference Raid.
3. Wire the loop into your own game through the [Integration API]({{ site.baseurl }}/docs/integration-api/).

## What the kit needs from you

- A Unity 6 project — **Unity 6 only** (6000.0 LTS and later 6.x). v1 does not support Unity 2022.3.
- Your own character controller. The kit ships none and never will: it integrates through a documented API and the included generic adapter (see [Integration API]({{ site.baseurl }}/docs/integration-api/)).
- Nothing else. The core is netcode-agnostic and compiles in a bare project with no controller and no transport package present.

## The honest frame, up front

Version 1 is a **solo loop with transport hooks**. It includes no multiplayer session, no matchmaking, no relay or server, and no hosted service of any kind — the hooks surface is there for your own networking code. Third-party controller adapters are not a verified v1 feature: v1 ships the generic adapter and the documented API. The full list is [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
