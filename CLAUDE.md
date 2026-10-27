# DINOSCORE RAPTOR CAPTOR ROGUE LITE - project rules (DINO-NNN)

Layered on Andrew's global `C:\Users\Andrew\.claude\CLAUDE.md`, which always wins on process and on the depth standard.

A coin-flip arcade roguelite for Steam. Sibling of REDEMPTION ALLEY (`D:\SKI BALL ROGUE LITE`). What the game is: `GAME.md`. The parts list: `SYSTEMS.md`. What is in flight: `NOW.md`.

## Session start, five steps

1. Global rules, this file and Auto Memory load automatically.
2. Read `GAME.md`, `SYSTEMS.md`, `NOW.md`.
3. Read the one file in `slices/now/` if there is one, and the spec file it names.
4. Run `python tools\check.py`. **Failures from last session get fixed before anything else.** If `BUGS.md` is over 40 lines, read the overflow out to Andrew and get a one-word ruling on each.
5. Say in one short paragraph, in player terms, what the next slice is. Get his go.

Nothing else is read. `kb/`, `methods/`, `decisions/` and `log/` open only when the slice in hand names one.

## During

- Work only on the slice in `slices/now/`. There is exactly one, ever.
- Anything else noticed goes to `BUGS.md` (one line) or `slices/next/` (a stub). Never folded into the current slice. **A related bug found next to the reported one is NAMED to Andrew and left alone until he says go.**
- Any decision that changes measured behaviour is written as PROPOSED the moment it surfaces, so it cannot evaporate. It is not built against until Andrew ratifies.

## Session end, seven steps, in order

1. Update the spec file the slice named. Same turn, not deferred.
2. Move the slice from `now/` to `done/`, set `Status: done`.
3. Rewrite `NOW.md`.
4. Update any `SYSTEMS.md` status word that changed.
5. Write `log/YYYY-MM-DD-NN-<topic>.md`, including the quoted-Andrew section.
6. Write any new decision body plus its index row, and execute any supersession in full, same turn.
7. Run `python tools\check.py` until it prints PASS. Then print the next-session prompt in chat, in a fenced block, as the last message. **Never write it to a file.**

**Andrew ends the session, not Claude.** Never self-wrap.

## The rules

- **DINO-001. A subagent is spawned for a SPEC-sized question. Never for a slice.** If the work fits in a `slices/` file, build it directly: no research pass, no delegated agent, no written analysis. If it needs a `spec/NN-*.md` written or substantially rewritten, a planning pass is allowed. Planning passes run as subagents via the Workflow tool, with independent context. A returned plan is a recommendation recorded as PROPOSED, never a lock.
- **DINO-002. Andrew is CEO. Recommendations are ungated, commitments are gated.** Research and forming a recommendation are done decisively. Anything hard to reverse (a locked concept, a paid tool, a Steam page, a scope lock, the theme, the name) waits for his explicit yes.
- **DINO-003. RETIRED 2026-08-03** (was: one file per session, deep-dive a `methods` or `kb` file). Retired by D-004. `methods/` and `kb/` are frozen reference, read when a decision touches their domain and named on the record when consulted. They are not grown as a per-session product. A documentation loop that produces no game is the wrong thing for a project aimed at a Steam launch.
- **DINO-004. Route look, feel, sound and art to the specialist agents.** This seat owns code, engine integration, data and logic. Visual art routes to the image-gen roster; code-powered look, motion, UI and sound route to Claude Design. Author the handoff prompt, port what comes back, never hand-build the sensory layer. Stage each handoff as one folder per prompt under `creative/handoff_outgoing/<topic>/` with `prompt.md` and copies of every attachment.
  - **INSPIRED BY, NEVER COPIED. Andrew, 2026-08-04.** The film references (TerrorVision, Brain Damage, The Thing, The Video Dead) are a source of visual GRAMMAR, not designs to reproduce. Take the palette, the grain, the lighting, the material and wetness language, the way a mouth opens, the sense of a thing that was BUILT. Never take a recognizable creature or character. A film's look is not protectable; a specific design is, and these four are among the most recognizable in horror. **Every research pass and every art prompt states which attributes are GENERIC to the era (free to use) and which are that design's SIGNATURE (to be avoided).** If a generated asset would make someone say "that is the creature from X" rather than "that feels like the era of X", it is wrong and gets regenerated.
- **DINO-005. No em dashes.** Anywhere, including outward copy. Commas, periods, parentheses, colons.
- **DINO-006. Capture a decision the moment it surfaces**, as a PROPOSED body plus its index row. Deferred defects go to `BUGS.md`, one line. There is no F-NNN sequence: slice numbers and D-NNN are the only two.
- **DINO-007. Follow the global rules first, and decide through the expert seats.** Consult the coupled seats in `methods/` before a decision in their domain, decide with that evidence, and name which were consulted. Andrew's eye plus the relevant seats sign off on look, feel and fun. Never this seat alone.
- **DINO-008. A ratified plan is a spec, not a starting point. Departures are two-tiered and go to ANDREW.**
  - **Tier 1, before any code is written:** the plan cannot run as written; a specified formula or value gives a wrong result taken literally; the plan conflicts with itself, a ratified decision, or the live build; a NEW constant, file, class, helper or config key is needed; an engine, performance or practicality wall forces a different approach; anything that changes measured behaviour. Stop, surface it, wait, implement the ruling verbatim, record a dated amendment.
  - **Tier 2, build it and flag it in chat the same turn:** the plan omitted a value any implementation must pick, an existing project constant is the null choice, no new constant, no design content, no behaviour change.
  - **When in doubt it is Tier 1.** "The engine forces it", "provably identical", "only an optimization", "one-line change", "documented in a comment" are each the CONTENT of the question, not a reason to skip asking. A code comment is not a flag; it is a silent deviation with a paper trail.
- **DINO-009. Delegation discipline.** Every pack is written to `packs/YYYY-MM-DD-<topic>.md` before dispatch and carries all nine spine sections with section 0 (how to answer) FIRST: how to answer, what the product is, the decision set, the seat positions quoted, hard constraints and blast radius, **dead ends already paid for**, what is built and green with measured numbers, the why-layer, the question. Hand over the investigation methods BY NAME (KISS, GRAYBOX, MICROSCOPE, BATMAN, TWO-STRIKE STOP); the agent cannot read these rules. **An agent READS; this seat WRITES.** Subagents never create, edit or delete files. Verify every load-bearing number against live source before recording it. **One focused issue per run**, the test being independent measurability. **Never auto-retry a failed subagent**: report the failure, the cause and the recommendation, and wait for Andrew's explicit go. **Never delegate diagnosis**; the main loop holds the instruments. Treat a subagent's AGREEMENT as weak evidence and its DISAGREEMENT as strong. Liveness comes only from the completion notification, never from a file size or a process check.
- **DINO-010. Nothing appends, except `BUGS.md`.** Every file is rewritten in place with a word budget, or is one file per item that is never read wholesale. Append-to-a-file-that-is-also-read is the shape that produced a 23,000-word ledger on the sibling and it does not exist here.
- **DINO-011. Nothing new at the repo root.** New content goes in an existing folder or it is not created. Root sprawl is how the sibling reached thirteen root files.
- **DINO-012. THIS IS A VIDEO GAME, NOT A PHYSICS SIMULATOR.** Andrew, 2026-08-04: "YOU ARE MAKING A VIDEO GAME. NOT A REAL WORLD PHYSICS SIMULATOR... THE SKEEBALL GAME BEING A RETARD OVER AND OVER." A postmortem of the sibling's 22 physics passes is in `log/2026-08-04-physics-spiral-postmortem.md`. Read it before tuning work.
  - **The disease is chasing a NUMBER instead of a PERSON, and the number does not have to be real.** Two thirds of the sibling's damage came from INVENTED internal gate targets, not from authenticity. A rule that only bans real-world derivation misses most of it.
  - **THE ONE HARD RULE: never two tuning or physics passes in a row without Andrew playing it.** The sibling ran four consecutive ratified physics amendments with nobody playing the build in between, because a green gate reads exactly like a validated build. It is not one. If he cannot play it, making it playable IS the next slice.
  - **The question to ask mid-task:** am I moving the machine to hit the target, or moving the target to match the machine? Moving a target so the physics can reach it is the turn. This will not catch everything, so it is a prompt to think, not a gate to pass.
  - **The cheap game-side fix is ALWAYS on the table and is never ruled out by process.** The sibling wrote "the geometry ladder runs to exhaustion first", and a geometry ladder has no end because geometry always offers one more lever. Worse: when Andrew SOFTENED a constraint, the project re-hardened it against him. **His softening is the ruling. Never argue him back toward the harder path.**
  - **A real-world fact from Andrew is a LOOK and LAYOUT instruction.** It does not oblige re-deriving everything downstream. When he says "the lane is flat" or "I have never seen a ball go dead", build that and move on.
  - **Automated checks stay** for what a person genuinely cannot see: determinism, containment, no double scoring, no lost coin. That is not the disease. The disease is a sweep standing in for a person on a question a person owns.
  - **NO NEW GATE SCRIPT FOR THIS RULE.** The sibling already mechanized this exact tripwire, and it failed three days ago on the very case it was written for. Adding machinery to a project with zero game code is the same pathology in a new costume.
  - **This outranks authenticity anywhere in this repo**, including any `kb/` figure or `spec/` Numbers table.

## The stack

- **Godot 4.7.1-stable**, at `D:\GODOT\Godot_v4.7.1-stable_win64.exe`. Physics: **Jolt**.
- **Two Jolt defaults silently break this game.** Set both explicitly in `project.godot`: `max_angular_velocity` 47.12 to **500.0** (the default caps the coin's spin) and `bounce_velocity_threshold` 1.0 to **0.05** (the default kills every rebound).
- **Verify in this order, both required:** `godot --headless --import` exits 0 FIRST, then `godot --headless --script tests/run_gut.gd`. A script-mode GUT run reports green while a broken native addon makes the editor unusable, because script mode never triggers GDExtension verification. **A green suite is not a green build.**
- **godot-mcp trap:** `add_node` silently drops Vector3 and Transform properties. Do geometry as text `.tscn` edits or procedurally, never through the MCP.
- **GDAI MCP plugin: do NOT install.** It crashed the sibling's import step on 4.7.1 with an access violation. Revisit only after the sibling resolves it.
- Assets: local RTX 3060 stack (ComfyUI/FLUX, Stable Audio, Blender) plus an owned Leonardo subscription, shared with the sibling. Meshy key shared (D-004).
- **Video settings are PLAYER OPTIONS, not a locked resolution.** Offer real display options that suit the monitor someone actually has. **The PS1 / PS2 / FMV look comes from the ASSETS: low-poly models, low-res textures, affine texture warping, vertex jitter, a limited palette, dithering and FMV grain.** It does not come from starving the render target, and it must not fight the player's hardware. Andrew, 2026-08-04. This supersedes the inherited 640x360 fixed target.
- Typed GDScript, warnings as errors.

## House style

No em dashes. Cite sources for factual, market, tooling and pricing claims. Only Andrew types the word RATIFIED.
