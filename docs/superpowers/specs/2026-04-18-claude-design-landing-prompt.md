# Claude Design — Landing Page Brief for DEVPACK

> Paste the prompt block below into Claude (design artifact mode / claude.ai / Figma Make).
> Everything above the `---` is context for you; everything below is the prompt to copy.

---

# PROMPT (copy from here down)

Design a landing page for **DEVPACK** — a collectible tabletop card game for developers. The vibe is "Gloomhaven for people who already work late." It is co-op, 1–3 players, 45–60 minutes per session. It is NOT a video game, NOT an NFT project, NOT a Magic clone. It is a physical card game with an optional AI-DM companion app.

## One-line pitch
*Every sprint is a session. Ship it, or die trying.*

## Core product truths the page must communicate

1. **It's a tabletop card game.** Physical cards on a table. The app is optional, not required.
2. **It's collaborative.** No PvP. You all win together or lose together.
3. **Six class decks** — Frontend, Backend, Data Science, DevOps, ML, Design — each plays mechanically different.
4. **AI-Dungeon-Master companion app** generates infinite missions and chaos events. Free, web-first.
5. **Chase cards are real devs** — Karpathy, Carmack, Grace Hopper, Linus, Margaret Hamilton. Autograph-tier 1/1 foils for charity.
6. **Loss is fun.** Fail a mission → earn "Tech Debt" cards that persist. The story of your career builds across sessions.

## Target audience
Developers, designers, PMs — the Hacker News / Lobsters / tech-Twitter crowd. They already play Slay the Spire, Gloomhaven, Pandemic. They own mechanical keyboards. They appreciate dry humor and real craft.

## Tone
- Dry, confident, self-aware.
- Uses real dev vocabulary without irony: *ship*, *incident*, *post-mortem*, *tech debt*, *standup ran long*.
- Not "fun startup" energy. Not "gamer" energy. Closer to Linear's tone: premium, calm, knowing.
- Zero corporate voice. Zero crypto/web3 vocabulary. Zero "revolutionize" or "unlock."

## Visual direction
- **Dark mode first.** Near-black background (#0A0A0A range). High-contrast typography.
- **Typography:** editorial. Pair a sharp display serif (think GT Super, Tiempos Headline) with a monospace for code-feel (JetBrains Mono, Berkeley Mono).
- **Card art as hero.** The cards are the product. Show them large, at angle, with subtle parallax. Foil-stamp Legends should shimmer on hover.
- **Grid-based layout**, asymmetric, generous whitespace. Feels like a print magazine for devs.
- **Accents:** a single saturated color — deep ember red (#E5553C or similar) for CTAs and emphasis. Everything else is grayscale.
- **No stock photography. No AI-generated hands typing on keyboards. No gradients.**
- Think: *Linear × Field Notes × the Criterion Collection.*

## Required sections (in order)

1. **Hero**
   - Logo wordmark (monospace, all-caps): `DEVPACK`
   - Below: the one-line pitch in display serif.
   - Below that: a short paragraph — 2 sentences, no more.
   - Primary CTA: **Join the waitlist** (email field, button, no password).
   - Secondary CTA: **Read the design notes** → links to a mock blog post about the game's mechanics.
   - Visual: a booster pack tilted 15°, foreground. Behind it, a Legend card mid-flip showing the foil stamp.

2. **"How it plays" strip**
   - Three columns: *Pick a class. Draw a mission. Ship it.*
   - Each with a tiny icon (thin-line, not emoji) and 10 words of copy.

3. **The six classes**
   - Horizontal scroll or grid. Each class as a card face showing:
     - Class name in display serif.
     - A 6-word tagline. ("Frontend — the combo artist." / "Backend — the tempo engine.")
     - A signature card preview.
   - Hover state reveals the class's signature-move card.

4. **"The Chase Tier"**
   - Mini gallery of Legend cards (Karpathy, Carmack, Hopper, Linus). 
   - Copy: "Foil-stamped. Numbered. Signed. Proceeds to ML-education nonprofits."
   - No prices. Tease only.

5. **AI-DM companion**
   - Mockup of a phone on a wooden table next to cards.
   - Copy: "The AI-DM runs the session so everyone plays. Free. Web-first. No login."
   - No download CTA (product isn't built yet).

6. **Playtest signup**
   - Form: email + "which city are you in?" + "have you played [Gloomhaven / Slay the Spire / Pandemic / none]?"
   - Copy: "We're running print-and-play sessions in Brooklyn, SF, and Berlin this summer."

7. **FAQ** (collapsible rows)
   - "Do I need the app?" → No. Game is complete without it.
   - "Is this an NFT?" → No. Physical cards, nothing on-chain, ever.
   - "Can I play solo?" → Yes. Solo is first-class.
   - "When can I buy it?" → Kickstarter late 2026. Waitlist gets 72-hour early access.
   - "Is this another Magic clone?" → No PvP, no combat, no mana.

8. **Footer**
   - DEVPACK wordmark + one-line manifesto: *"A tabletop card game for people who ship."*
   - Links: Twitter/X, Instagram, email, press kit (mock).

## Interactions to include

- Email waitlist form that POSTs to `/api/waitlist` (stub — just log and thank-you state).
- Class cards should have a subtle 3D tilt on hover (CSS transform, not a library).
- Legend cards in the Chase Tier section reveal foil texture (gradient overlay) on hover.
- Smooth scroll, snap sections on desktop.
- Respect `prefers-reduced-motion`.

## Tech preferences
- Single HTML artifact, Tailwind for styling, vanilla JS for interactions.
- Fonts from Google Fonts or Adobe Fonts CDN — specify your choice.
- Mobile-responsive, obviously. Design mobile-first if that's how you naturally work.

## What NOT to include

- No testimonials (we don't have any yet).
- No pricing.
- No "As seen on" press logos.
- No countdown timer.
- No newsletter cross-sell beyond the single waitlist form.
- No "Built with Claude" footer or AI-generated badge.
- No emoji. None.

## Deliverable
One self-contained responsive landing page, ready to drop onto Vercel. Include placeholder card art as tasteful SVG or CSS illustrations — do not attempt to AI-generate card art; leave clear placeholder slots labeled `[card art: Karpathy Legend]` etc. so real illustration can be swapped in later.

Go.
