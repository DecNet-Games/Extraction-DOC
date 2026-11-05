# PUSH NOTE — Extraction-DOC (built 2026-11-05, local only, NOT pushed)

## What this folder is

The complete, push-ready source tree for Extraction Loop & Stash Kit's documentation site, built to the Decnet house "-DOC" pattern (structure/config mirrored from MergeGuard-DOC / AgentProof-DOC / ShipSheet-DOC):

- Just the Docs Jekyll site via `remote_theme` (no `theme:` gem key, no `just-the-docs` gem in the Gemfile — the pairing that fixed the two known GitHub Pages errors: "The just-the-docs theme could not be found" and "The github-pages gem can't satisfy your Gemfile's dependencies").
- 21 content pages: Home + Getting Started + Installation + Quick Start + The Home Window + One-Click Setup + The Stash + Raid State Machine + Settlement + Insurance + Traders & Economy + Persistent Saving + Integration API + Transport Hooks + Reference Raid — Greyline Depot + Economy Config + What v1 Is Not + FAQ + Troubleshooting + Changelog + Support.
- **No media in this tree, by design** (the MergeGuard-DOC precedent: documentation never ships invented imagery, and pages are written so they do not depend on any image). Screenshots join `assets/` only after real captures exist — Extraction's Session A screen grabs are failure evidence only (a foreground console covered ~93% of every frame) and are not used.
- Content sourced ONLY from the verified record: the prep listing copy (`../../extraction-prep/LISTING-COPY.md` — fence-clean; every capability line is one of its verified claims) and the build verification it carries (57/57 EditMode + 2/2 PlayMode on Unity 6000.5.4f1, bare-project compile verified, Reference Raid PlayMode-proven solo). Three fences are load-bearing throughout: **v1 is solo play + transport hooks only** (no multiplayer/session/matchmaking/relay/server claim anywhere), **third-party controller adapters are not claimed** (generic adapter + documented API only; bridge components called out as unverified starting points), and **Unity 6 only** (2022.3 explicitly unsupported). The Home window's own line "Multiplayer demo unavailable: NGO is not installed" is documented as the solo-configuration report it is.
- No product Asset Store URL exists yet (no portal draft yet — draft creation is capture-gated in the programme), so Home/Installation link the Decnet Games publisher page (118262) — swap in the product URL after the listing goes live, as with the other -DOC trees.

## Exact repo to create

- **Name:** `Extraction-DOC`
- **Owner:** `DecNet-Games` (GitHub org account)
- **Visibility:** public (required for GitHub Pages on this setup)
- **Live URL once Pages is on:** https://decnet-games.github.io/Extraction-DOC/ (matches the `baseurl: "/Extraction-DOC"` already set in `_config.yml`)

## Push route (do this from the laptop, per the standing no-card-spam rule)

Bulk pushes go via laptop git over SSH — never the GitHub connector.

1. BOSS creates the empty repo `DecNet-Games/Extraction-DOC` on GitHub (no README, no .gitignore — this tree carries its own).
2. Copy this folder's contents to the laptop clone location, then: `git init` (if needed) → `git add .` → `git commit` → the final `git push` is BOSS's own ~10-second action at his terminal (laptop git credentials only work interactively — known constraint).
3. On GitHub: repo **Settings → Pages → Build and deployment → Source: GitHub Actions** (the standard github-pages workflow), or "Deploy from a branch" → `main` / root if Actions is unavailable. The other -DOC repos run on the same org setup — mirror whichever source they use.
4. After the first successful build, verify:
   - the live URL loads with the Just the Docs theme (no theme error),
   - nav order: Home, Getting Started, Installation, Quick Start, The Home Window, One-Click Setup, The Stash, Raid State Machine, Settlement, Insurance, Traders & Economy, Persistent Saving, Integration API, Transport Hooks, Reference Raid — Greyline Depot, Economy Config, What v1 Is Not, FAQ, Troubleshooting, Changelog, Support.
5. Only after the site is live: apply the house-format description (`../DESCRIPTION-HOUSE.md`) to the portal draft when it is created — its link line carries `DOCUMENTATION → https://decnet-games.github.io/Extraction-DOC/` (dead-link rule: never publish the link before the site resolves).

## What remains

- Repo creation + push + Pages enable: BOSS-side steps above (by design — this build stopped at a complete local tree, per instructions).
- Media: after the capture reshoot produces usable frames into `../raw/`, real frames can be added under `assets/images/` with a small content update — not required for the site to be complete or correct.
- Portal draft: does not exist yet (capture-gated); the house description waits for both the draft and this site being live.
- Nothing in the tree itself: content, config and Gemfile are complete and internally verified (page count, front matter, nav order checked against disk).
