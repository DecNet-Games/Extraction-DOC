---
layout: default
title: Economy Config
nav_order: 16
description: "The economy is data: trader stock, prices and margins are data assets, the insurance fee and return delay are configured values, and settlement reads your economy config as an input."
---

# Economy Config
{: .no_toc }

The kit's economy is tuned through **data and config**, not code edits — because settlement takes your economy config as one of its three inputs (raid record, stash, economy config), changing the config changes outcomes in a way you can test deterministically.

## What is data

- **Trader definitions** — stock, prices and margins are data assets (see [Traders & Economy]({{ site.baseurl }}/docs/traders-and-economy/)). Add a trader or re-price one without touching the loop.
- **Insurance terms** — the fee and the return delay are configured values. Shipped defaults: **15 percent** fee, return after **one raid cycle** (see [Insurance]({{ site.baseurl }}/docs/insurance/)).
- **Item data** — footprints, stackability, and values live on the items themselves (see [The Stash]({{ site.baseurl }}/docs/the-stash/)).

## Tuning with the simulation

Because settlement is deterministic, the shipped **100-raid economy-integrity simulation** doubles as a tuning instrument: change the config, run the simulation, and read whether the economy still holds together — before your players run the experiment for you.
