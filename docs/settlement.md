---
layout: default
title: Settlement
nav_order: 9
description: "Settlement is a deterministic function of the raid record, the stash, and your economy config, and it produces an itemized record: kept, lost, insured-pending, sold, and fees."
---

# Settlement
{: .no_toc }

When a raid ends — extraction or death — the **settlement engine** closes it. Settlement is where an extraction game keeps or breaks its promises, so the kit makes it boring in the best way: readable, and repeatable.

## The itemized record

Every settlement produces a record with the outcome itemized:

- **Kept** — what came home to the stash.
- **Lost** — what the raid cost (on death: everything uninsured that was carried).
- **Insured-pending** — insured items lost on death, now scheduled for return (see [Insurance]({{ site.baseurl }}/docs/insurance/)).
- **Sold** — what was converted to currency.
- **Fees** — what the raid charged (insurance fees and the like).

Nothing moves without a line. If a player asks "where did my rifle go?", the record answers.

## Deterministic

Settlement is a **deterministic function of the raid record, the stash, and your economy config** — the same inputs always produce the same record. That property is load-bearing: it makes your economy **auditable**, your support answers provable, and your balance changes testable. The kit's test suite includes a **100-raid economy-integrity simulation** built on exactly this property.

Settlement is not an anti-cheat or server-authority system — see [What v1 Is Not]({{ site.baseurl }}/docs/what-v1-is-not/).
