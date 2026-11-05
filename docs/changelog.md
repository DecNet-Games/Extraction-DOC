---
layout: default
title: Changelog
nav_order: 20
description: "Extraction Loop & Stash Kit 1.0.0 — the initial release: Tetris-grid stash, raid state machine, deterministic settlement, insurance, traders, persistent saving, integration API, transport hooks, and the Reference Raid."
---

# Changelog
{: .no_toc }

## 1.0.0 — initial release

- Extraction Loop Home — one Editor window: status strip, Welcome with one-click setup, Stash Board preview, Raid Loop, Traders & Insurance, Samples & Scenes, Documentation & Support.
- Tetris-grid stash core: shaped items (width × height footprints), 90-degree rotation, stacking, placement validation with plain-language rejection reasons.
- Raid state machine: InStash, Deploying, InRaid, Extracted, Died, Settlement — one legal path for every raid, with an itemized raid record.
- Lose-on-death settlement: itemized kept / lost / insured-pending / fees record, produced by a deterministic settlement engine.
- Insurance: bought at deploy time, scheduled for return after a configurable delay (shipped default 15 percent fee, one raid cycle), tracked as a visible pending-returns list.
- Trader and economy layer: data-driven trader definitions, atomic quote-then-confirm buy/sell, one sample trader (Depot Trader).
- Persistent saving: one versioned JSON save document (stash, currency, pending returns, trader deltas, statistics) with atomic write, last-good backup recovery and a schema migration chain.
- Integration API plus a generic adapter (conformance-suite proven) for wiring the loop to the controller you already use.
- Transport hooks surface: a netcode-agnostic core with a hooks assembly your own transport code can subscribe to. Solo play only in v1 — no multiplayer, session, or matchmaking ships.
- Reference Raid — Greyline Depot: a solo playable sample scene that runs the full loop (stash, deploy, loot, extract, settlement, trader).
- Documentation set: quick-start, integration guide, API reference, economy and insurance reference, "what v1 is not".
- 57 automated EditMode tests + 2 PlayMode tests (NUnit), including a 100-raid economy-integrity simulation — Unity 6.
