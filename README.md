# DEVPACK

> A tabletop card game for people who ship.

Concept site and design archive for **DEVPACK** — a co-op, deck-based tabletop card game where 1–3 developers race to ship a product before the sprint ends. Six class decks that actually play different, a free AI Dungeon Master, and collectible chase cards of real devs.

**Live site:** https://rdsciv.github.io/devpack

---

## Status

Pre-alpha concept. Game design is locked. Landing page is live. Physical product is in pre-production; print-and-play playtesting begins summer 2026. Kickstarter targeted for late 2026.

## What's in here

```
.
├── index.html                             # Single-file landing page (HTML/CSS/vanilla JS)
├── docs/superpowers/specs/
│   ├── 2026-04-18-devpack-tcg-design.md   # Full game design spec
│   └── 2026-04-18-claude-design-landing-prompt.md
└── README.md
```

## Run locally

Zero build step. Zero dependencies. It's one HTML file.

```bash
git clone https://github.com/rdsciv/devpack.git
cd devpack

# Pick any static server
python3 -m http.server 8000
# or: npx serve .
# or just: open index.html
```

Then visit http://localhost:8000.

## Design notes

Typography: **Fraunces** (variable serif, editorial) paired with **JetBrains Mono** (wordmark, meta, card rules).
Palette: ink `#0C0B0A`, warm paper `#F4EBDC`, vermillion ember `#C23B28`, foil gold `#C89B4A`.
No tracking. No analytics. No third-party scripts. No service workers. Respects `prefers-reduced-motion`.

The game design spec lives in [`docs/superpowers/specs/2026-04-18-devpack-tcg-design.md`](docs/superpowers/specs/2026-04-18-devpack-tcg-design.md) — read that first if you want the full mechanical picture.

## Roadmap

- [x] Game design spec
- [x] Landing page (concept)
- [ ] Waitlist backend (currently stubbed to `console.log`)
- [ ] Print-and-play PDF (Set 1: "Ship It", Frontend + Backend classes)
- [ ] In-person playtest sessions: Brooklyn, San Francisco, Berlin, Austin
- [ ] AI-DM companion app (separate project)
- [ ] Card art commissions
- [ ] Kickstarter campaign — targeted late 2026

## Contributing

Not yet. The design is still under active iteration and we're not accepting external mechanical changes. If you have a card idea, bug report, or playtesting interest, join the waitlist on the live site or open an issue.

## License

Website code (`index.html`, CSS, JS): **MIT** — do what you want with the technical bits.
Game design, card names, rules text, flavor text, logos, and art: **© 2026 DEVPACK · All rights reserved.**

This split is deliberate. The code is a landing page scaffold anyone can learn from; the game is a product we're building.

## Press

`press@devpack.game` · press kit coming once we have one worth sending.
