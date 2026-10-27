# Systems

The parts list. One row per part, one paragraph each. A part gets a `spec/` file only when it leaves `not started`. Status words: `not started`, `spec`, `building`, `done`.

| # | Part | Status | Spec |
|---|---|---|---|
| 01 | The flip gun | building | `spec/01-the-flip-gun.md` |
| 02 | The target wall | building | `spec/02-the-target-wall.md` |
| 03 | The floor spinner | building | `spec/03-the-floor-spinner.md` |
| 04 | The run | building | `spec/04-the-run.md` |
| 05 | Coins (the deck) | building | `spec/05-coins.md` |
| 06 | Mods and charms | building | `spec/06-mods-and-charms.md` |
| 07 | The shop | building | `spec/07-the-shop.md` |
| 08 | Tickets (the in-run currency) | building | `spec/08-tickets.md` |
| 09 | The operator modes | spec | `spec/09-operator-modes.md` |
| 10 | Art | not started | - |
| 11 | Sound | not started | - |
| 12 | Saving | not started | - |
| 13 | The juice (score feedback) | building | `spec/13-the-juice.md` |

**01. The flip gun.** The controller and the entire skill axis. A coin is laid flat, a spring lever sets power, the barrel tilts and slides laterally, the trigger fires. Everything the player does happens before the trigger; after that it is physics and watching. Release must be deterministic, so all shot-to-shot variance lives downstream in part 02. This is the first thing built, because if the throw is not fun nothing else matters.

**02. The target wall.** The vertical back wall of sculpted creature mouths the coin is flipped at. FOUR mouths at launch, stacked vertically with the smallest highest and worth most (500, 300, 200, 20), which the inventor's own patent confirms. Each mouth is a different creature drawn from one of the four film references: TerrorVision, Brain Damage, The Thing, The Video Dead. Inspired by, never copied (DINO-004). Also owns the hot or lit target and the jackpot cluster. A coin that fails every mouth falls to part 03.

**03. The floor spinner.** A wide flat living table at the base, dotted with numbered holes, swept by one slow rotating arm above it (D-008: the table is FIXED, the arm turns). Every coin the wall did not take lands here, so the floor is a second scoreboard rather than a safety net. Where a coin rests decides its score; the arm only decides when you find out, so there is no timing to wait out. Hole count, values and sweep rate are all data, because the roguelite corrupts all three. Its art is ORIGINAL, subordinate to the four wall mouths.

**04. The run.** The session shape: rounds, coins per round, and the scoring window (the real machine's Mode 006 theme delay, a timer that runs after the coin leaves the gun) as the round clock. Owns the quota ladder and its growth rate, the fail state, and the between-round sequence. About 30 to 45 minutes per run.

**05. Coins (the deck).** Coins are the deck units, the equivalent of the sibling's balls. Mass, bounce, tumble bias, value multipliers, splitters. Drawn per round, bought and removed between rounds.

**06. Mods and charms.** Mods attach to a target or a spinner trough and change what it is worth or what it does. Charms bolt onto the cabinet and change global rules. Together they are the build. Effects use ring or target SELECTORS, never value literals, so content stays data.

**07. The shop.** Built graybox (D-015): a between-nights buy-button pause, purchases wired to the build and reset on death. Rarity pricing, reroll, sell-back, removal and buying coins are follow-ups.

**08. Tickets.** The single IN-RUN currency (D-015 revised the old cosmetic-only law): earned by clearing a night, spent between rounds, reset on death so run power is earned by play.

**09. The operator modes.** The distinctive hook, and the one thing no comparable roguelite has. The real cabinet exposes a service menu (Modes 004 to 039) where the operator sets per-target point values, ticket payout ratios and timer delays, adjusted with MODE, RESET, UP and DN buttons. The player gets into it and corrupts it. This is a progression ladder disguised as a maintenance panel and is where the theme's possession arc should land hardest.

**10. Art.** PS1 and PS2 era low-poly plus CRT, VHS and FMV grime, one room, one cabinet. **The era look is carried by the ASSETS, not by a locked resolution:** low-poly models, low-res textures, affine texture warping, vertex jitter, limited palette, dithering, FMV grain. Video settings stay player-selectable so the game suits whatever monitor someone has. Blocked on D-003, the theme and name. Routes to the image-gen roster and Claude Design per DINO-004, never hand-built here.

**11. Sound.** The cabinet's voice: the spring, the coin ring, the funnel swallow, the spinner's endless turn, the operator panel's beeps. Routes to Claude Design as portable WebAudio per DINO-004.

**12. Saving.** Run state, meta progression, unlocks, settings. Deliberately last: nothing is worth persisting until the run loop is proven fun.

**13. The juice (score feedback).** The dopamine layer that plays the scoring breakdown as escalating number pops, the readout rolling up, the creatures reacting, screen shake and CRT pulse, and sound. Godot built, sound to Leonardo, presentation only so it never changes a score.

---
Overview: `GAME.md`. In flight: `NOW.md`.
