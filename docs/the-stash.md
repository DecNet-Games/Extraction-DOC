---
layout: default
title: The Stash
nav_order: 7
description: "A Tetris-grid stash: items occupy width-by-height footprints, rotate in 90-degree steps, and stack where their data says they stack. Placement is validated, and rejections say why."
---

# The Stash
{: .no_toc }

The stash is where your players' gear lives between raids — a **Tetris-grid inventory**, not a list.

## Shaped items

Every item occupies a real **width × height footprint** on the grid: a rifle is long, a medkit is square, ammunition is small. Items **rotate in 90-degree steps** to fit the space they have, and **stack where their data says they stack** — stackability is item data, not a global switch.

## Placement validation

Every placement is validated — **bounds, overlap, fit** — before anything moves:

- A valid placement applies.
- A **rejected placement changes nothing** and **says why in plain words**: out of bounds, overlapping an occupied cell, no fit at that rotation. Your UI can show the reason directly; your players never lose an item to a silent refusal.

## The Stash Board

The [Home window's]({{ site.baseurl }}/docs/home-window/) Stash Board preview renders your demo profile's live stash, so the grid you tune in the Editor is the grid the loop settles into after a raid. What the settlement adds or removes lands here — see [Settlement]({{ site.baseurl }}/docs/settlement/).
