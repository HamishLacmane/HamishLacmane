# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## What this is

Hamish's personal portfolio/landing page — the top of the whole Hamilin family tree (Lacmane → Hub → Cards/Star/Guide, see the hierarchy note in the [[project_hamilin_sites]] memory). A static site, no framework, no build step, no package.json — `index.html` + `styles.css`, same zero-dependency pattern as every other Hamilin repo. Deploys to GitHub Pages with zero configuration.

Lives under Hamish's personal `HamishLacmane` account (not the old `hlacmane` org from ~10 years ago at `github.com/hlacmane/hlacmane.github.io`) — deliberate choice, matches where every other Hamilin repo already lives. **That old repo must not be pulled from or referenced** — Hamish was explicit about this.

## Design — first real build, 2026-08-19

Deliberately minimal: name big and centered (Bahnschrift display font, matching the wordmark treatment used across Hub/Guide/Star), everything else stacked below it, vertically centered in the viewport. **Colour scheme undecided** — plain black/white/grey only (`--ink`/`--ink-soft`/`--ink-muted`/`--hairline`), same "explicit neutral placeholder, not a real choice" pattern already used on Hamilin Star. Don't treat these as final brand colours.

Content, top to bottom:
- **Name**: "Hamish Lacmane", `<h1>`.
- **Social icons**: LinkedIn (`linkedin.com/in/hamish-lacmane-7b080b107`) and GitHub (`github.com/HamishLacmane`), inline Tabler Icons SVG (MIT licensed, no CDN — same technique as Guide's restaurant icons), 40px.
- **"Personal Projects" section** (small uppercase label, `.section-label`): The Third Wheel FM (`thethirdwheel.netlify.app`, mic icon), Hamilin Hub, Hamilin Star (⭐ prefix — same emoji as Star's own favicon), Hamilin Guide (📕 prefix — same emoji as Guide's own favicon). All open in a new tab.
- **Separate block below a hairline divider**: "My Squash Level" (`app.squashlevels.com/player_detail?player=534743`, ping-pong icon) — not a "project", kept visually distinct.

**Favicon**: "HL" monogram, same inline-SVG-`data:`-URI technique as Star's ⭐ and Guide's 📕 (dark rounded-square background, white bold initials) — chosen because this page is literally just the name, so initials fit better than a topic emoji. Easy to swap later if Hamish wants something else.

## Still to do

- **Holographic card idea** — Hamish wants some kind of holographic card element on the page eventually. Raised 2026-08-19 as a "for the todo" idea, not specced or built. Ask for details (what it displays, where it sits) before attempting.
- Colour scheme — undecided, see above.
- No favicon confirmation from Hamish yet on the "HL" monogram choice — built as a reasonable default, flag if he wants something else.

## Git workflow

Local commit email set to `16271451+HamishLacmane@users.noreply.github.com` (not `--global`) — see [[user_github_noreply_email]] memory, same as every other Hamilin repo; pushing with the real email gets a GH007 rejection since Hamish has "block command line pushes that expose my email" enabled. No LICENSE file by design (all rights reserved). No `Co-Authored-By: Claude` trailer on commits, matching every other Hamilin repo. `gh` CLI not installed — push the feature branch and hand Hamish the GitHub "create PR" URL GitHub prints on push.
