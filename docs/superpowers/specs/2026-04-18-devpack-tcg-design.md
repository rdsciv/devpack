# DEVPACK — Game Design Spec

> **Working title:** DEVPACK · "Ship It" (Set 1)
> **Format:** Physical tabletop card game, co-op, 1–3 players, ~45–60 min/session
> **Optional companion:** Mobile AI-DM app (web-first)
> **Audience:** Developers, designers, PMs, tech-adjacent hobbyists who already play Gloomhaven / Slay the Spire / Pandemic
> **Date:** 2026-04-18

---

## 1. Elevator Pitch

You and up to two teammates are devs racing to ship a product before the sprint ends. Each player runs a class deck — Frontend, Backend, Data Sci, DevOps, ML, Design — with genuinely different mechanics, not reskins. Every turn the DM (a human friend or a free AI-DM app) throws Chaos at you: flaky tests, scope creep, prod is down, the PM "just has one more ask." You play cards to push the Ship Track before the Bug Track overflows. Win or lose, the story of the sprint becomes your character's career arc, persisting across sessions.

**Tagline candidates:** *Ship it, or die trying.* · *The tabletop RPG for people who already work late.* · *Every sprint is a session.*

---

## 2. Design Pillars

1. **Collaborative, never competitive.** No PvP mechanics, ever. You all win or all lose. This is the differentiator from every other TCG.
2. **Classes feel genuinely different.** A reviewer must be able to say "Frontend plays nothing like Backend." Mechanical identity > flavor-text identity.
3. **Infinite replay via AI-DM.** The physical game is complete without the app. The app unlocks unbounded Mission + Chaos generation, so the game never runs out of scenarios.
4. **Tabletop-first.** Plays great on a table with zero tech. Photographs well. TikTok-friendly session lengths. The app is icing, not infrastructure.
5. **Collectibility is mechanical, not speculative.** Chase cards (Legends, Repos, Bugs) have real game impact. They're not just shiny holos.
6. **Loss is fun.** A failed mission gives you a "Tech Debt" card — a persistent negative in your deck until a future mission clears it. Loss tells a story.

---

## 3. Core Loop (One Round)

1. **DM reveals a Chaos card.** Flavor + mechanical effect. If AI-DM, it's generated; if human DM, drawn from the Chaos deck.
2. **Players take turns.** Each turn:
   - Draw up to hand size (5).
   - Play 1–2 cards. Cards resolve into the Ship Track (progress), the Bug Track (damage), or both.
   - Spend Focus tokens (the single resource) if a card costs them. Tokens regenerate 2/turn.
   - Optionally trade a card with an adjacent player (the "pair program" action — 1/round team-wide).
3. **Check tracks.** If Ship ≥ Mission Goal, you win. If Bug Track overflows, you lose (but earn XP + a narrative stinger).
4. **Advance the round counter.** If rounds run out before Ship fills, mission fails — but partial completion earns partial rewards (tiered outcomes below).

**Turn feels like:** draw → read the Chaos → play a combo → hand the phone/DM prompt to the next player. ~3 minutes per player per round.

---

## 4. Tiered Win/Loss Outcomes

Not binary. Every mission resolves into one of five outcomes, each with narrative flavor and mechanical consequence:

| Outcome | Condition | Reward |
|---|---|---|
| **Shipped Clean** | Ship filled, Bug Track below halfway, rounds remaining | Full XP, rare card draft, "Legendary Sprint" career note |
| **Shipped** | Ship filled before rounds ran out | Full XP, common card draft |
| **Shipped With Debt** | Ship filled on the final round OR Bug Track above halfway | Reduced XP, one "Tech Debt" card added to deck |
| **Missed Deadline** | Rounds ran out, Ship 50–99% full | Reduced XP, two Tech Debt cards, narrative stinger |
| **Incident** | Bug Track overflowed | No XP, three Tech Debt cards, BUT earn a "Post-Mortem" card — a one-shot powerful card for your next session |

Incident grants the single strongest item in the game. Losing is the setup for a comeback.

---

## 5. The Six Class Decks

Each class ships with a 30-card starter deck. Mechanics are distinct — not just different art.

### 5.1 Frontend — *The Combo Artist*
- Low individual card strength, high combo potential.
- Core mechanic: **Chain.** Playing a card with Chain triggers the "on next play" effect of the previously chained card.
- Feels like: Slay the Spire Silent, setup → payoff.
- Signature card: **"Ship the Hero Section"** — if you chained 3+ cards this turn, +6 Ship.

### 5.2 Backend — *The Tempo Engine*
- Slow start, late-game snowball.
- Core mechanic: **Persistent Infrastructure.** Play infrastructure cards that stay on the table and generate 1–2 Ship per round passively.
- Feels like: Dominion/builder-engine energy.
- Signature card: **"Stand Up the Service"** — costs 3 Focus, persists, generates 2 Ship/round.

### 5.3 Data Science — *The Filter*
- Draws too many cards, discards most, finds the one that matters.
- Core mechanic: **Query.** "Peek the top N, keep 1, shuffle the rest." Cards often have "search" effects.
- Feels like: card-advantage control.
- Signature card: **"Run the Query"** — peek top 5 of any deck, keep 1, shuffle rest.

### 5.4 DevOps — *The Shield*
- Defensive enabler. Makes the team unkillable.
- Core mechanic: **Absorb.** Reduce Chaos damage or prevent it entirely. Shield tokens.
- Feels like: Pandemic's Medic + healer.
- Signature card: **"Rollback"** — negate the last Chaos card. Exhaust after use.

### 5.5 ML / AI — *The Probabilistic Bomb*
- High-variance power. Roll cards or reveal deck tops; effects scale with luck.
- Core mechanic: **Training Run.** Reveal top 5 of your deck; if 3+ share a type, massive effect.
- Feels like: gambling, but with a win-more curve.
- Signature card: **"Converge"** — if training run succeeds this turn, +8 Ship and draw 3.

### 5.6 Design — *The Reframer*
- Utility/manipulation. Turns problems into progress.
- Core mechanic: **Reframe.** Move tokens between tracks, modify other players' cards, convert Bug Track into Ship Track at a penalty.
- Feels like: Magic's Azorius control / toolbox.
- Signature card: **"User Story Rewrite"** — convert 3 Bug into 2 Ship.

**Why six?** Four feels thin for a collectible property; six gives two product expansions post-launch (see §11). Launch with **Frontend + Backend** only.

---

## 6. Card Types

1. **Skill cards** — your class's signature abilities. Drive mission progress.
2. **Tool cards** — shared across classes. "ChatGPT Assist," "Stack Overflow," "Senior Engineer Slack Ping," "Copilot Autocomplete." Usually cost Focus but are high-impact.
3. **Vibe cards** — meta-mechanical. "Rubber Duck Debug" (untap Focus), "Coffee Break" (+1 hand size for 2 rounds), "Log Off For The Day" (skip a Chaos card, lose a round). These are the emotional heart.
4. **Legend cards** — collectible chase. Real devs, real impact. See §8.
5. **Repo cards** — artifact relics. Often powerful but situational. See §8.
6. **Bug cards** — villains. Live in the Chaos deck. Real CVEs. See §8.

---

## 7. The Three Decks

### Mission Deck (15 in starter box)
- Each mission is a scenario card: Goal (Ship target), Round limit, special rules.
- Examples:
  - **Ship the MVP** — 20 Ship, 8 rounds, standard Chaos. Tutorial mission.
  - **Legacy Migration** — 30 Ship, 12 rounds, 2× Chaos deck.
  - **Viral Launch** — 15 Ship, 5 rounds, but Ship target +1 every round (scope creep).
  - **Demo in Two Days** — 25 Ship, 6 rounds, every player starts with a Tech Debt card.
  - **Crunch Week** — 40 Ship, 10 rounds, hand size −1. Reward on win is doubled.
  - **Black Friday** — 20 Ship, 6 rounds, Bug Track overflow at 10 (half normal).
  - **Rescue the Codebase** — 15 Ship, 7 rounds, every Ship card also deals 1 Bug. Cleanup mission.

### Chaos Deck (30 in starter box)
- Drawn at the start of each round.
- Examples:
  - **Flaky test blocks merge** — +2 Bug.
  - **Designer changed their mind** — Design-class cards cost +1 this round.
  - **Prod is down** — pause Ship progress until a player plays a DevOps card.
  - **PM walks over** — Ship target +3 immediately.
  - **Standup ran long** — each player skips their first card this turn.
  - **Your laptop dies** — one random player discards 2 cards.
  - **Good vibes** — +3 Ship, no downside (rare positive).
  - **It's Friday** — end of round, all players draw 2.

### The Chase Tier (mixed rarity)
- Legends, Repos, Bugs. Pulled from boosters, not starter box (except 5 starter-tier Legends in the box).

---

## 8. Chase Cards (Collectibility Tier)

These are the cards people post on Instagram.

### 8.1 Legends (real devs, real impact)
Each Legend is playable in any class. Powerful, flavorful, 1–2 per deck max.
- **Karpathy** — once per game: peek top 5 of any deck, keep one.
- **Carmack** — this turn, all your cards cost 0.
- **Grace Hopper** — reshuffle the Bug Track into the Ship Track. (Clutch 1/game.)
- **Fabrice Bellard** — play any number of cards this turn, ignore normal limits.
- **Linus** — reject one Chaos card; replace with a Chaos card of the DM's choice from the discard. Flavor: "NAK."
- **DHH** — draw 3, then each player may discard a Tool card to draw 1.
- **Rich Hickey** — all persistent Backend infrastructure outputs doubled this turn.
- **Margaret Hamilton** — prevent the next Incident this session. Exhaust.
- **Guido** — all Python-themed cards (Data Sci, ML) cost −1 this turn.

Tiered rarity: common Legend (5/set), rare Legend (3/set), ultra-rare foil 1/1 numbered-signed (charity tie-in).

### 8.2 Repos (artifact relics)
- **torvalds/linux** — DevOps permanent; +1 to all Absorb effects.
- **tensorflow/tensorflow** — ML synergy; doubles next Training Run.
- **leftpad** — cursed; play to remove any Tool card from the team's pool for the rest of the session. Useful and ironic.
- **Bitcoin whitepaper** — 1/1 ultra-rare chase; converts 1 Bug into 5 Ship. Numbered print run.
- **openai/gpt-2** — discard 1 card, generate its "echo" — a random card of the same cost from any class deck.

### 8.3 Bugs (villain tier, in Chaos deck)
- **Log4Shell** — skip all Tool cards for 2 rounds.
- **Heartbleed** — each player reveals hand; DM removes one card from each.
- **Left-Pad Incident** — all shared Tool cards are unavailable this round.
- **Y2K** — Ship Track requirement +4 immediately.
- **Therac-25** — one random player takes 5 Bug damage directly. Grim.

Flavor text reads like a baseball card: *CVE-2021-44228 · Severity 10.0 · Affected: Everyone.*

---

## 9. Persistence — The Career Log

Every player has a Career Log (paper sheet in starter box; digital in AI-DM app).

**Tracked:**
- Sessions played, missions shipped, incidents survived.
- XP and career level: **Junior → Mid → Senior → Staff → Principal → Distinguished.** Each level unlocks a Signature Move card.
- Deck customization: earned cards slot into the starter 30. Deck stays 30 cards (swap in, swap out).
- Tech Debt carried forward. Debt is removed by winning specific missions ("Refactor Week," "Hire a Senior").
- Narrative stingers from dramatic wins/losses ("You shipped with 17 seconds left." / "The AWS us-east-1 outage was your fault.")

**Career milestones unlock:**
- Junior → Mid: 1 Signature Move card.
- Mid → Senior: Signature Move upgrade + access to rare Tool cards.
- Senior → Staff: Cross-class hybrid cards (e.g., "Principal Engineer" dual-class card).
- Staff → Principal: A 1/1 custom "Legendary You" card the app generates from your session history. This is the hook.
- Principal → Distinguished: Prestige reset with a permanent bonus.

---

## 10. AI-DM Companion App

**Scope (MVP):**
- Free web app. Phone-sized UI. No login required; optional account for persistence.
- Generates Mission cards: LLM prompts structured against a schema (Goal, Round Limit, Special Rules, Flavor).
- Draws Chaos: randomized from the physical deck OR generated with flavor tied to the current mission.
- Tracks Career Log across sessions for all players at the table.
- Hosts card-metadata lookup (scan-later QR layer).
- Stretch: voice mode — the AI-DM narrates Chaos cards aloud.

**Explicitly NOT in MVP:**
- Full digital version of the game (never — tabletop-first).
- Card-trading marketplace.
- API-key redemption plumbing (deferred).
- Cryptographic provenance / on-chain anything.

**Monetization surfaces (future):**
- Premium mission packs (themed: "FAANG Layoffs," "Crypto Winter," "The AI Gold Rush").
- Sponsored missions (e.g., Vercel-themed mission pack).
- Career Log cloud-save for subscription.

---

## 11. Product & Release Roadmap

### Set 1: "SHIP IT" (launch)
**Starter Box — $49 retail:**
- 2 class decks (Frontend + Backend), 30 cards each
- 15 Mission cards, 30 Chaos cards
- 5 starter-tier Legends
- 2 dual-sided Track boards
- Focus tokens, round counter
- Rulebook with quickstart
- 3 paper Career Log sheets
- AI-DM app launch code

**Booster Pack — $6 retail:**
- 10 cards: 6 common, 2 uncommon, 1 rare, 1 chase-tier (Legend/Repo/Bug)
- 1 scratch-off insert (placeholder for future API-key mechanic; at launch, scratch-off reveals a cosmetic digital card unlock)

### Set 2: "AGENT ERA" (Q2 post-launch)
- Adds **ML class deck**, AI-themed Legends (Hinton, Bengio, LeCun, Hassabis), expanded Chaos ("RLHF drift," "hallucination reported on HN").

### Set 3: "OPEN SOURCE" (Q3)
- Adds **DevOps + Data Sci** class decks, Linux/Git/Python Legends, Repo-tier expansion.

### Set 4: "INCIDENT" (Q4)
- Crisis-focused missions, Bug tier expansion, the Therac-25 / Challenger / Knight Capital disasters.

### Set 5: "BROWSER WARS" (Y2)
- Adds **Design** class, 90s/00s nostalgia, Hardware Legends slot in.

### Set 6: "RETRO" (Y2)
- Hardware Legends (C64, Altair, iPhone, Jetson), cross-set bonus cards.

---

## 12. What Makes This A Hit

1. **Solo viability.** Reviewers play solo first. If solo is good, BGG rating > 7.5 becomes achievable.
2. **Session length.** 45–60 min is the sweet spot for repeat plays. Gloomhaven's 2-hour sessions are a barrier; we undercut that.
3. **Class feel.** Six genuinely different classes = six collection arcs = six reasons to buy.
4. **Infinite replayability via AI-DM.** Solves the "we've seen every Chaos card" drop-off that kills Pandemic-likes.
5. **Cultural resonance.** The Legend/Bug/Repo cards reward people who know the history. Karpathy signing charity 1/1s at NeurIPS is a launch headline.
6. **Loss is fun.** Tech Debt + Post-Mortem cards make losing the most memorable version of the game.
7. **Vocabulary.** "Ship It" / "Incident" / "Tech Debt" / "Signature Move" — these phrases are already in players' mouths.

---

## 13. Explicit Non-Goals (YAGNI)

- No PvP / no battle mode.
- No app-required play. The game must work with zero tech.
- No NFTs, no on-chain provenance, no crypto.
- No real-money trading markets at launch.
- No "digital twin" of the game. Physical-first, forever.
- No card-game balance patches. Errata only, rarely. This is a finished object, not live ops.

---

## 14. Open Risks (to track, not solve here)

1. **Six-class balance is hard.** Plan for an 8-week blind playtest phase per set.
2. **Legend licensing.** Start with living legends who have charity causes. Do not ship a Legend without written consent.
3. **Bug card tastefulness.** Therac-25 killed people. Flavor text must be respectful. Have a legal/ethics read before print.
4. **AI-DM latency.** Target <2s generation per Chaos card; pre-generate a buffer each round.
5. **Tabletop-first means retail distribution.** Retail requires Asmodee/Z-Man-class distribution or a strong DTC + crowdfunding channel (Kickstarter is the obvious play for Set 1).

---

## 15. Next Steps (outside this spec)

1. **Landing page + waitlist** — hand off to Claude design with a focused prompt (see accompanying prompt artifact).
2. **Print-and-play prototype** — 2 classes × 30 cards × printable PDF. Get 20 playtesters in 30 days.
3. **Kickstarter prep** — based on playtest signal.
4. **AI-DM app prototype** — separate spec, separate plan.
5. **Sponsor outreach** — after playtest proves the core loop works.

---

*End of spec. This is a product + game design document, not a software implementation plan. Next artifact is a Claude-design brief for the landing page + waitlist site.*
