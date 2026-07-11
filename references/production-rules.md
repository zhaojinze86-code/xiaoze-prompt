# Production rules

## Capacity audit

For each scene, calculate:

- spoken characters and intended delivery rate;
- named pauses and natural breaths;
- silent reactions that carry plot information;
- blocking and prop interaction time;
- establishing and transition time;
- number of speakers, locations, and fragile actions.

Classify the result as `fits`, `tight`, or `overloaded`. A clip is overloaded when natural performance, clear cuts, or stable lip-sync cannot coexist within 15 seconds.

## Stability priorities

Prioritize in this order unless the story demands otherwise:

1. Character identity and correct speaker.
2. Dialogue intelligibility and lip-sync.
3. Story beat and performance endpoint.
4. Screen direction and continuity.
5. Camera motion.
6. Background complexity and decorative atmosphere.

Reduce camera motion, crowd behavior, hand activity, and secondary effects before sacrificing identity or dialogue.

## Shot grammar

- Establishing shot: 0.6-1.5 seconds for fast short drama, longer only when geography matters.
- Speaker shot: stable medium close-up or close-up, one named speaker, one mouth assignment.
- Listener reaction: 0.6-2 seconds depending on narrative weight.
- Evidence insert: 0.8-2 seconds, preserve exact geometry and placement.
- Internal monologue: lips closed; permit visual cutaways while one voice continues.
- Hard cut: state the exact local timestamp and destination shot.

## Continuity ledger

Track immutable identity anchors separately from transient scene state.

Immutable anchors include face, apparent age, build, hair, signature wardrobe, and voice identity. Transient state includes pose, gaze, breath, injury phase, prop hand, current emotion, open motion vector, camera phase, and audio phase.

Accepted footage overrides planned state. Never build a continuation from a rejected take. Record the observed tail before finalizing the next prompt.

## Modification log categories

- `技术性调整`: duration, cuts, camera feasibility, lip-sync, stability, physics, continuity, or prompt precision without changing story meaning.
- `创作性调整`: dialogue wording, event order, motivation, reveal, character intention, or emotional outcome.
- `一致性修正`: names, voice identity, wardrobe, props, geography, or latest user-approved canon.

For every item, state the original, revised version, reason, production effect, and story impact.

