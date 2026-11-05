---
layout: default
title: Transport Hooks
nav_order: 14
description: "A netcode-agnostic core with a hooks assembly your own transport code can subscribe to. v1 is solo play plus these hooks: no session, no matchmaking, no relay, no server ships."
---

# Transport Hooks
{: .no_toc }

The kit's core is **netcode-agnostic**: all loop logic lives in a transport-free data core. That is a verified property, not an aspiration — the package is proven by **compiling it in a bare project with no controller and no transport package present**.

## What ships

A **hooks assembly** exposes **raid-state replication payloads** for your own transport code to carry: when the raid state machine moves, the hooks surface publishes the payloads your networking layer can subscribe to and send however your game already sends things.

## What does not ship — stated plainly

Version 1 is a **solo loop with transport hooks**. It includes:

- **no multiplayer session**,
- **no matchmaking**,
- **no relay or server**,
- **no hosted service of any kind**.

The hooks surface is there for your own networking code, and **the kit makes no promise about it**: synchronising the loop across machines, with your transport, your authority model, and your testing, is your game's work. When the optional multiplayer demo dependency is absent, the [Home window]({{ site.baseurl }}/docs/home-window/) says so outright — "Multiplayer demo unavailable: NGO is not installed" — and the kit runs in its solo configuration.
