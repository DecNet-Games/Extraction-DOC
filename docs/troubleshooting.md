---
layout: default
title: Troubleshooting
nav_order: 19
description: "The states the kit reports about itself: a rejected placement and why, a rejected state transition in the log, the solo-configuration line, a recovered save, and a pending return that has not landed yet."
---

# Troubleshooting
{: .no_toc }

The kit's failure states are reported states — each one names what happened. These are the ones you will meet.

## An item will not go into the stash

Placement is validated — bounds, overlap, fit — and a **rejected placement changes nothing and says why in plain words**. Read the reason: rotate the item (90-degree steps), free the cells it overlaps, or check its footprint against the grid edge. Nothing was moved or lost by the attempt. See [The Stash]({{ site.baseurl }}/docs/the-stash/).

## The log shows a rejected transition

Your integration code made a call that is illegal in the raid's current state (extracting after death, settling before the raid ended, deploying twice). The transition was **rejected and logged**, and the raid state is uncorrupted. Fix the calling order against the state machine: InStash → Deploying → InRaid → Extracted / Died → Settlement. See [Raid State Machine]({{ site.baseurl }}/docs/raid-state-machine/).

## The window says "Multiplayer demo unavailable: NGO is not installed"

The optional multiplayer demo dependency is absent, and the kit is running in its **solo configuration** — v1's designed state, reported honestly rather than hidden. It is not an install failure: v1 is a solo loop with transport hooks. See [Transport Hooks]({{ site.baseurl }}/docs/transport-hooks/).

## The save loaded from backup

The save document failed to load cleanly, so recovery loaded the **last-good backup and reported it**. Your loop state is the backup's state — nothing was silently emptied. If this repeats, inspect the document for external edits; the write path itself is atomic. See [Persistent Saving]({{ site.baseurl }}/docs/persistent-saving/).

## An insured item has not come back yet

Returns land **after the configured delay** (shipped default: one raid cycle) and sit in the **pending-returns list** until they do — check the list in the Home window's Traders & Insurance section. An item still inside its delay is on schedule, not lost; when it lands, it lands exactly once. See [Insurance]({{ site.baseurl }}/docs/insurance/).
