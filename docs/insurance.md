---
layout: default
title: Insurance
nav_order: 10
description: "Insure gear at deploy time for a configured fee — shipped default 15 percent, return after one raid cycle — tracked in a visible pending-returns list until it lands back in your stash, exactly once."
---

# Insurance
{: .no_toc }

Insurance is the promise that softens death: pay a fee before the raid, and a lost favourite comes back.

## How it works

1. **Buy at deploy time.** Insurance is bought as the raid deploys, for a **configured fee** — the shipped default is **15 percent**, with return after **one raid cycle**. Both values are your economy config, not constants (see [Economy Config]({{ site.baseurl }}/docs/economy-config/)).
2. **Die.** Settlement marks the insured items **insured-pending** and schedules their return (see [Settlement]({{ site.baseurl }}/docs/settlement/)).
3. **Track the return.** Scheduled items sit in a **visible pending-returns list** — in the [Home window's]({{ site.baseurl }}/docs/home-window/) Traders & Insurance section — until they land.
4. **Receive, exactly once.** The item lands back in your stash **exactly once — never duplicated, never vanished**. Exactly-once is a tested property of the kit, not a hope: a duplicated insured weapon would be an economy exploit, and a vanished one a broken promise.

## The Reference Raid demonstration

The [Quick Start]({{ site.baseurl }}/docs/quick-start/) runs the whole arc: insure the starter rifle, extract once, then die on purpose in the second raid and watch the insured rifle come back through the pending-returns list.
