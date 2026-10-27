# BUGS - DINOSCORE RAPTOR CAPTOR ROGUE LITE

> One line per deferred code defect or side-issue. Layered on global + project CLAUDE.md.

- 2026-08-07 FIXED (Andrew: "corect same as mouths"): the floor pockets vanished a scored coin on contact; now they land-then-swallow like the mouths (floor.gd `_swallow`, SWALLOW_SECONDS 0.5). Score still latched on entry, GUT 53/53.
- 2026-08-07 OPEN: tools/test_check.py cannot run -- its C2 fixture copies slices/next/001 and 002, which moved to done/ sessions ago (FileNotFoundError), so the gate's self-tests abort before any check. Pre-existing, unrelated to today's work; the real gate check.py passes. Fixture paths need to be made robust to slice movement.

- 2026-08-04 FIXED: R cleared nothing. No coin joined the "thrown" group, so main.gd iterated an empty list. Named to Andrew during slice 003, fixed on his go.

## Revision Log

- 2026-07-29: created at Phase 0 scaffold.
- 2026-08-08 DEFERRED (slice 012): Mouth 2 TerrorVision creature is glossy (baked Meshy highlights vs the matte-outside R3 rule) and still uses the old skull -15deg dress tilt; polish when slice 011 (mouths come alive) re-touches mouths. Backend untouched, Mouth 2 = 200 confirmed.
- 2026-08-08 DEFERRED (008): the rigging engine shipped graybox with 3 starter items (Feed/Blob/Lure) + the coin Stage 3, proving all five stages and legible stacking; the rest of the D-014 pool (complex mods The Descent/The Wicker Man/etc., more charms, operator modes, cursed deals) is future content, data-only via the EffectDef registry.
- 2026-08-09 DEFERRED (juice inc 3, Andrew chose defer): the CRT scanline/chroma PULSE (second half of inc 3) waits for the art pass (part 10). No CRT shader exists in the graybox yet to pulse; the plan assumed one. The screen shake (inc 3 first half) shipped.
- 2026-08-11 DEFERRED (economy later increment): the FREE between-rounds pick (pick 1 of 3, no tickets) is not in slice 009's base loop. Andrew's trigger idea: it fires at CHECKPOINT rounds or RANDOMLY, not every round. Build after the base shop is play-signed; cut it if it reads as clutter.
