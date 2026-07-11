---
name: xiaoze-prompt
description: Analyze Chinese drama scripts and reference prompts, then produce production-ready live-action Seedance 2.0 shot plans and LibTV prompts. Use when the user invokes /xiaoze-prompt or $xiaoze-prompt, supplies a script or AI-generated prompt, requests shot breakdowns, character and scene bibles, dialogue timing, speaker-aware cuts, camera revisions, voice/performance direction, continuity planning, or needs every generated clip kept within a 15-second limit with an explicit modification log.
---

# Xiaoze Prompt

Turn a script into executable live-action Seedance 2.0 clips for a LibTV-first workflow. Treat user-supplied prompts as references, not immutable instructions.

## Project defaults

- Target realistic live-action people, natural skin texture, physically motivated light, restrained acting, and stable faces/hands.
- Use Seedance 2.0 as the generation model and LibTV as the primary orchestration workflow.
- Enforce a hard maximum of 15 seconds per generated clip. Choose shorter clips when the dramatic beat benefits.
- Preserve the latest user correction over earlier pasted drafts. Flag name or continuity conflicts instead of silently reverting them.
- Permit changes to shots, camera, dialogue pacing, blocking, and prompt wording when they improve story clarity or generation stability. Always report every change.

## Required workflow

1. Read the full supplied scene before drafting prompts.
2. Identify the dramatic function, conflict, hidden intent, story outcome, and emotional progression.
3. Build or update character, voice, scene, prop, wardrobe, screen-direction, and continuity records.
4. Measure dialogue, actions, pauses, reactions, and transitions against the available duration.
5. Split the scene into clips of at most 15 seconds. Give every clip one narrative job and a clear opening and ending state.
6. Design the edit before writing prose prompts. Cut to the active speaker before their line; cut to the listener for the reaction after the line.
7. Write exact shot IDs and local time ranges starting at zero for each generated clip. Mark every transition explicitly, such as `1.2秒直接硬切`.
8. Generate a detailed Seedance 2.0 director prompt and a compact LibTV execution prompt.
9. End with a modification log comparing the user's source with the delivered version.
10. For connected clips, mark future prompts provisional until the previous accepted take or actual final frame is reviewed.

## Timing rules

- Do not equate the 15-second ceiling with a target duration.
- Budget Mandarin dialogue by actual delivery: roughly 3-4 characters per second for natural speech and 2-3 for slow emotional delivery, then add explicit pauses and reactions.
- Keep emotional pauses only when they change meaning. Remove decorative silence.
- Give physical actions preparation, execution, consequence, and a visible endpoint.
- If dialogue and performance cannot fit naturally, split the clip or propose a clearly logged dialogue compression. Never solve overload only by rushing speech.
- Read [references/production-rules.md](references/production-rules.md) for the complete capacity and stability checklist.

## Speaker and edit rules

- When the speaker changes, cut to the new speaker unless a deliberately motivated off-screen line is requested.
- The speaking shot must name exactly who produces lip movement. State that all other visible characters keep their mouths closed.
- After important dialogue, cut to the listener's reaction when that reaction carries story information.
- For internal monologue, keep the character's lips closed. The voice-over may continue across cutaways to evidence, another character, or the environment.
- Use direct hard cuts by default for interrogation and short-drama dialogue. Do not hide cuts behind vague wording such as `随后看到`.
- Maintain the 180-degree line, eyelines, left/right geography, prop placement, light direction, and action phase across cuts.
- Prefer separate generation nodes for fragile multi-shot sequences. If using one multi-shot generation, state the exact cut times and forbid continuous long-take interpretation.

## Performance and voice

- Translate emotions into visible behavior: breath interruption, blink rate, gaze shift, jaw tension, grip, posture, or a held pause.
- Bind every line to a named character, voice identity, emotion strength, pace, emphasis, subtext, and mouth state.
- Treat timbre and delivery as separate layers. A cold character may deliver a superficially gentle line without losing the underlying voice identity.
- Preserve the same voice identity across the project while allowing story-state changes such as weakness, guilt, injury, or concealment.
- Avoid generic `电影感`, `高级感`, exaggerated villain delivery, theatrical ancient-drama cadence, plastic skin, and unsupported emotional adjectives.

## Camera and realism

- Give each shot a scale, angle, lens feel, camera move, speed, subject relationship, and endpoint.
- Use one motivated primary move per short shot. Split incompatible move stacks into separate shots.
- Keep dialogue and lip-sync shots stable; avoid orbits, rapid head turns, and busy hand choreography.
- Convert poetic atmosphere into physical light, material, weather, and sound. For example, render `烛火森冷` as warm practical flames contrasted with cool environmental light rather than blue flames unless fantasy is intended.
- Use wide shots to establish geography, medium close-ups for dialogue, close-ups for decisive reactions, and inserts for evidence or props.

## Output contract

Return, in this order:

1. Capacity verdict: source time, estimated playable time, overloads, and chosen clip split.
2. Dramatic analysis.
3. Required character cards and voice identities.
4. Required scene, prop, wardrobe, and continuity settings.
5. A clip map with source timeline, generated duration, narrative job, opening state, and ending state.
6. For every clip: shot-by-shot timecode, scale, angle, lens, camera, blocking, performance, dialogue, speaker, mouth-state, sound, and exact hard-cut points.
7. A natural-language Seedance 2.0 director prompt.
8. A compact LibTV execution prompt and recommended node names.
9. The modification log: original, revision, reason, effect, and whether story meaning changed.
10. A request for the accepted clip or actual final frame before locking the next continuation prompt.

Use the reusable formatting skeleton in [references/output-template.md](references/output-template.md). Do not omit cut points merely because the prose already names different speakers.

