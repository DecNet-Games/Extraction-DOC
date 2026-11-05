---
layout: default
title: Quick Start
nav_order: 4
description: "The ten-minute path: run setup, then play the Reference Raid — stash, insure, deploy, loot, extract, settle — and run it again to watch insurance return your rifle after a death."
---

# Quick Start
{: .no_toc }

1. TOC
{:toc}

## 1. Open the Home window

**Tools → Decnet Games → Extraction Loop & Stash Kit** opens the one window everything lives in: a status strip, Welcome, Stash Board preview, Raid Loop, Traders & Insurance, Samples & Scenes, Documentation & Support.

## 2. Run the one-click setup

Setup is one click, is safe to re-run, and reports in plain language — including, honestly, when the kit is running in its solo configuration. Full detail: [One-Click Setup]({{ site.baseurl }}/docs/one-click-setup/).

## 3. Open the Reference Raid

From **Samples & Scenes**, open **Greyline Depot** — the shipped solo playable scene that runs the full loop. Full detail: [Reference Raid — Greyline Depot]({{ site.baseurl }}/docs/reference-raid/).

## 4. Stash, insure, deploy

On the Stash Board, choose the **starter rifle and medkit**. Insure the rifle at deploy time. Deploy: the raid state machine moves InStash → Deploying → InRaid, and your insured gear is now at risk — and on record.

## 5. Loot and extract

Loot the **two salvage crates**, then extract. The settlement engine produces the itemized record — kept, lost, insured-pending, sold, fees — and your loot lands in a stash that visibly grew. Full detail: [Settlement]({{ site.baseurl }}/docs/settlement/).

## 6. Run it again — and die on purpose

Deploy again and let the raid kill you. The uninsured gear is lost and the settlement says so, line by line. The insured rifle is scheduled for return, tracked in the pending-returns list — and it comes back, exactly once. Full detail: [Insurance]({{ site.baseurl }}/docs/insurance/).

That is the whole product, demonstrated with shipped materials only. Wiring the same loop into your own game is the [Integration API]({{ site.baseurl }}/docs/integration-api/).
