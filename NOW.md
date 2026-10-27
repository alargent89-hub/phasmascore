# Now

## Current slice
**015 the shot becomes a skill shot** (`slices/now/015-the-shot-becomes-a-skill-shot.md`).
C (coin weights) is DONE and play-signed. B (the mouths) is HALF done: the art is built and
placed; the collision, launch tuning, and animation remain. Spec: `spec/02-the-target-wall.md`.

## State
All green (import 0, GUT 118/118, check.py PASS). Committed: `0bd584d` (the wall dressed +
laid out + camera reframed) on top of `18d1c95` (weights, economy, combo, readability, mouths).

## Built this stretch
- **C, coin weights (D-017, PROPOSED, play-signed).** The gun is a SPRING: a heavier coin
  launches slower, a lighter one faster, so one power can't fit every coin. House 0.05, Dead &
  Buried 0.065 (HEAVY), new Poltergeist 0.04 (LIGHT); HEAVY/LIGHT HUD tags.
- **Two END NIGHT fixes:** clicking it no longer fires a coin (fire moved to _unhandled_input)
  or hangs 8s (early-end short settle).
- **Coin readability:** loaded coin flush on the launcher, a LOADED name label, rack highlights
  the selected coin with its name.
- **B art:** three Meshy mouths built (The Thing 500, Brain Damage 300, Video Dead 20), dressed
  onto the wall over the untouched scoring geometry, laid out with Andrew (~20 passes + harsh
  critic subagents). Camera reframed to -6deg so the full wall is in frame. `--shot` debug
  capture (nohud/grey/side) added for tuning from renders.

## TOP NEXT (Andrew's direction, this seat's sequence)
Finish B: **collidable mesh geometry, then tune coin launches into the mouths, then animations
(screen juice + some as obstacles).** THE HIGHEST-RISK ZONE (the sibling's 22-pass scar). Order:
1. **OPEN with a planning pass (DINO-001 subagent)** on real mesh collision that keeps scoring
   intact (the 0/100 trap) + obstacle geometry. Rewrites `spec/02`.
2. **Real mouth collision, ONE mouth first, scoring Sensor/cup untouched.** Andrew plays it.
3. **Tune the launch into the mouths.** ONE lever per pass, Andrew plays between EVERY change,
   two-strikes-stop (DINO-012). Guardrail (D-010): openings stay >= 2 coin diameters; obstacles
   make the cup hard to REACH, never smaller.
4. **Animations, layered:** idle juice (breathing) -> eyes (glued-on objects: blink/roll/glow)
   -> real mouth open/close (two-state mesh or rig, an asset call) -> animated obstacles.

## Debt (the #1 flagged item)
Specs lag: spec/01 (spring launch + gun reset + power bar), spec/05 (weights), spec/02 (mouths
dressed + layout), spec/04/06/13, spec/07+08 to author. methods §7 rewrite. D-011 aim-reset
extension. D-015 uppercase RATIFIED token is Andrew's to type. Camera reframe wants a play.

## The calendar
`methods/methods-production.md`. Next Fest 14-21 June 2027; launch 20 July 2027.
