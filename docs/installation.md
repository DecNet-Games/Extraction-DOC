---
layout: default
title: Installation
nav_order: 3
description: "Install Extraction Loop & Stash Kit from the Unity Asset Store and run the one-click setup. Sold exclusively through the Unity Asset Store. Unity 6 only."
---

# Installation
{: .no_toc }

## Asset Store only
{: .no_toc .text-delta }

Extraction Loop & Stash Kit is sold and delivered **exclusively through the Unity Asset Store** (publisher: Decnet Games). There is no other download channel, no licence server, and no account to create — if a copy of the kit came from anywhere else, it did not come from us.

## Install

1. Purchase Extraction Loop & Stash Kit on the Unity Asset Store.
2. In Unity, open **Window → Package Manager**, select **My Assets**, download and import the kit into your project.
3. Open the window from **Tools → Decnet Games → Extraction Loop & Stash Kit**. Everything the kit does in the Editor lives in that one home window — see [The Home Window]({{ site.baseurl }}/docs/home-window/).
4. Run the [one-click setup]({{ site.baseurl }}/docs/one-click-setup/) once. Setup is safe to re-run and reports in plain language.

## Requirements

- **Unity 6 only** (6000.0 LTS and later 6.x), verified on Unity 6000.5.4f1 with clean-project and bare-project installs. **v1 does not support Unity 2022.3.**
- No other package is required: the kit's core compiles with no controller and no transport package present (bare-project compile is part of the verified record).
- Your own character controller for your game — the kit integrates with it; it does not replace it (see [Integration API]({{ site.baseurl }}/docs/integration-api/)).

## Verified state

Automated verification for v1.0.0, on **Unity 6000.5.4f1**: 57/57 EditMode tests and 2/2 PlayMode tests green, including a 100-raid economy-integrity simulation; the Reference Raid scene is playable solo and PlayMode-proven end to end.
