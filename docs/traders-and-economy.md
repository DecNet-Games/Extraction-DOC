---
layout: default
title: Traders & Economy
nav_order: 11
description: "Data-driven trader definitions with atomic quote-then-confirm buy and sell: funds and items move together or not at all, and the charged amount equals the quoted amount. One sample trader ships: the Depot Trader."
---

# Traders & Economy
{: .no_toc }

Traders turn salvage into currency and currency into gear. In the kit, the trader layer is **data, not code**.

## Data-driven definitions

Trader **stock, prices and margins are data assets**. Adding a trader, restocking one, or re-pricing an economy is a data edit — no code change, no recompile of the loop. One sample trader ships with the kit: the **Depot Trader**, wired into the Reference Raid so the buy/sell path is exercised end to end.

## Atomic quote-then-confirm

Every transaction runs in two steps:

1. **Quote** — the trader states the price: this item, this amount.
2. **Confirm** — funds and items **move together or not at all**, and **the charged amount equals the quoted amount**.

There is no state in which the player paid and received nothing, or received and paid nothing, and no drift between the price shown and the price charged. Those are the two failure modes that make players distrust a game economy; the transaction shape removes both.

Trader activity is part of the persisted loop state — trader deltas are written into the save document (see [Persistent Saving]({{ site.baseurl }}/docs/persistent-saving/)).
