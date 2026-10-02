# PUNCHLINE - production and design notes

Working recommendation, prepared 2 October 2026. This is pre-jam design documentation, not a claim that the game exists or has been playtested.

## Why this concept

The selected direction is a **3D pop-up comic book**: comic panels unfold into small playable city dioramas with authored room cameras. The player can see the entire hook in one action: twist a printed BAM!, illuminate it, and watch its new direction launch a character or a prop. Comic, Twist and Light all affect gameplay. The set's depth supports moving around obstructions, pushing props across the room and launching onto raised ledges. A capped force system can be reused for traversal and prop puzzles, while compact comic panels keep content manageable.

The visual target is [the AI-generated concept mockup](docs/concepts/punchline-3d-concept.png), not an implemented scene. Build the impression from a reusable paper-city kit, expressive character poses, ink contours, orange force graphics, cyan flash effects and brief authored transitions. Decorative detail and camera flourishes may be simplified; the gameplay remains 3D.

The important risk is feel: an exciting written pitch does not establish that launches are fun. The first development milestone is a representative challenge with excellent input, clear feedback and reliable recovery. We will adjust range, impulse, collision shapes and difficulty within the proposed premise rather than add systems to compensate.

## Agreed constraints and open facts

- Team size: five. The user reports broad engine/language skills.
- No concept or proposal has been submitted through the official form yet. The public repository is https://github.com/varunpatil5050/punchline.
- User says the development window begins at midnight after proposal submission. Treat midnight at the end of 2 October as 3 October, 00:00 IST for planning only. If that is the official Hour 0, 100 hours ends 7 October, 04:00 IST. Confirm the final deadline with the event's Discord announcements.
- Game code, mechanics and architecture begin at official Hour 0. Before then, prepare the concept, paper layouts, proposal and administrative submission.
- The announcement assigns the proposal 15%; the supplied screenshot assigns 10% to a cropped plan-compliance label. Their relationship is unconfirmed. Ask the organizers through Discord; do not invent a scoring formula.
- Team registration, track eligibility and required Discord team-thread membership remain unconfirmed.
- Varun Patil / varun.patil@students.iiit.ac.in / @varunp685 is the only supplied member record.

## Core interaction contract

These are design rules to implement after the jam begins, not prebuilt system code.

1. Snap moves across a 3D ground plane and obeys simple gravity. WASD/arrows are relative to the authored room camera, whose angle remains stable during active input. A sound-word launch provides the jump.
2. Mouse picking selects one visible word within finite distance of Snap and with unobstructed world-space line of sight from the camera prop. Selection is stable, visibly outlined and limited to one word. Cursor visibility does not let the player target through a physical obstruction.
3. Q/E changes its orientation by a quarter turn within the plane indicated by its visible rotation ring. A horizontal ring offers four directions across the room; a vertical ring offers up, down and two sideways directions. The ring's orientation is authored independently of whether the word is anchored on a floor or wall. A visible world-space arrow gives the exact force direction; the stationary trigger-zone outline identifies affected bodies. Rotation itself causes no impulse.
4. A flash activates only that selected word. Bodies intersecting the zone receive the same authored impulse for their body class. Cap velocity to prevent accidental tunneling or unlimited stacking.
5. A short automatic flash recharge prevents unintended repeated firing; tuning must not turn into waiting. Never require repeated rapid clicking for a puzzle solution.
6. Crates use constrained motion and simple collision. Avoid unstable stacks, tiny contact points, hidden depth requirements and solutions depending on numerical simulation quirks. Broad platforms and restrained diagonal movement must keep launches readable.
7. Leaving safe bounds or entering a static hazard returns Snap to the current panel checkpoint. R restores Snap, props, switches and word orientations to the panel's authored start state.
8. A clearly marked exit advances the panel. Display progress and preserve completed panels within the session; the full short game must be completable without persistent storage.

## Eight challenge sketches

These are paper designs, not verified playable levels. During development, record starting layout, reachable areas, a demonstrated solution, likely wrong moves and restart behavior for each.

| Challenge | Introduces | Intended reasoning | Main test |
| --- | --- | --- | --- |
| 1. First Flash | Upward BAM! | Stand in the zone; flash; land on a broad exit ledge. | A new player discovers the action in under a minute. |
| 2. Wrong Way | Quarter turns | Rotate a sideways word upward before launching. | Arrow and zone update together; no precision aim required. |
| 3. Between the Lines | 3D line of sight | Move around a fixed obstruction in depth to illuminate the word. | A blocked target gives clear feedback; camera exposes the useful route. |
| 4. Special Delivery | Horizontal rotation ring, crate and switch | Turn a word toward a crate; shove it across the room onto a broad plate. | A failed shove is recoverable; no unstable stacking. |
| 5. Step Up | Prop positioning | Place a crate as a step to reach the next launch zone. | Crate position remains predictable. |
| 6. Double Feature | Two words | Set directions, launch to a safe landing, then activate the next word. | No required midair rotation or rapid clicking. |
| 7. Off Script | Order matters | Position a prop first, then reuse the launch route without blocking the exit. | Wrong order is obvious and a reset is immediate. |
| 8. The Last Laugh | Finale | Redirect the villain's large printed punch to open the final route. | All rules are familiar; ending works without a new system. |

The sequence must earn its 10-15 minutes through discovery and mastery. Do not pad it with walking, repeated puzzles, long dialogue or mandatory wait timers. Adjust challenge layouts from observed first-play times.

## Five suggested ownership tracks

Ownership is tentative until the team assigns names. One person owns each shared scene or system to avoid conflicting edits.

| Owner | Responsibilities | Integration agreement |
| --- | --- | --- |
| 1. Direction and integration | 3D movement feel, authored camera framing, scene flow, integration and final creative decisions. | Own player, view camera and application shell; review core merges. |
| 2. Targeting and force mechanics | 3D picking/line of sight, rotation, flash, affected-zone feedback, crate response and reset state. | Publish the word/prop behavior contract before others author levels. |
| 3. Levels and playtests | Eight layouts, tutorial clarity, challenge progression and first-play observations. | Use shared components; avoid adding new mechanics in individual levels. |
| 4. Art and UI | Reusable 3D paper-city kit, character design/poses, palette, comic effects, panels, menus and accessibility presentation. | Deliver consistent dimensions and collision-independent visuals; reuse scenery across rooms. |
| 5. Audio and release quality | Music/SFX, browser export, itch.io packaging, credits and independent completion checks. | Establish a hosted build early; maintain a known working release. |

The 100 hours are elapsed event time, not a request for anyone to work continuously. Arrange overlapping handoffs and sleep so integration and quality checks remain reliable.

## Milestones and contingency

| Hours | Expected state | If behind |
| --- | --- | --- |
| 0-8 | One convincing challenge, repeatable launch and browser export. | Simplify collision, range and force behavior while keeping the locked interaction. |
| 8-24 | Complete gameplay loop, reset, transitions and early hosted build. | Remove optional animation/dialogue and protect the core loop. |
| 24-48 | Full challenge sequence assembled. | Simplify weak layouts; use shared art rather than new systems. |
| 48-64 | Beginning-to-credits game. | Stop adding content types; make the existing sequence complete. |
| 64-82 | Timed fresh-player tests and polish. | Fix recurring confusion and failure recovery first. |
| 82-92 | Feature freeze and release testing. | Completion blockers and performance issues only. |
| 92-100 | Released playable, final documents and submission buffer. | Preserve the known working build; verify the official form and public access. |

## Judging evidence

| Supplied criterion | Evidence we will aim to demonstrate |
| --- | --- |
| Theme interpretation - 20% | The same interaction visibly uses printed comic words, twisting and light. |
| Gameplay/mechanics - 30% | Responsive launch, readable consequences, varied authored challenges and a satisfying finale. |
| Technical stability - 20% | Hosted browser completion, reliable reset, broad landing areas and no completion blockers. |
| Audiovisual cohesion - 20% | A small shared palette, comic type/ink language, tightly timed effects and consistent sound. |
| Plan compliance - 10% shown | Delivered mechanics and scope match the submitted proposal. The screenshot label is cropped. |

## Planned technical approach

Godot 4 + GDScript is the working choice. Use the Compatibility renderer and single-threaded web export. Compatibility supports core 3D features and is the renderer available for Godot's web target; see the official [renderer overview](https://docs.godotengine.org/en/stable/tutorials/rendering/renderers.html). Verify the installed stable version and export templates at Hour 0, and test a representative 3D room on itch.io during the first eight hours. Export choices follow the official [Godot web export documentation](https://docs.godotengine.org/en/stable/tutorials/export/exporting_for_web.html), accessed 2 October 2026.

Prioritize small scene bounds, few materials, simple collision and a reusable scenery kit. Budget lights and transparent effects deliberately. Test the actual chosen outline/ink presentation in Compatibility before applying it to every asset. Advanced rendering features are not part of the proposal. Benchmark the busiest room on a team reference laptop before content production expands; reduce decoration and effect cost if performance or launch clarity suffers.

Export directly as index.html and package the generated files together without renaming them. itch.io's HTML5 upload requires index.html, all required files in the ZIP, correctly cased filenames and relative asset paths. See [itch.io HTML5 documentation](https://itch.io/docs/creators/html5), accessed 2 October 2026.

Use a Start button so audio begins from a user action. Test fresh sessions, browser focus changes, fullscreen/resizing, missing persistent storage and sound off. Keep the launch effect accessible with reduced flash intensity and reduced shake.

## Submission material

The public repository has been created with a MIT license and the draft two-page proposal.pdf in its root. Before proposal submission: fill all five member records, choose the team name/track, review the premise, replace the draft PDF with the final proposal, complete the official form and confirm Discord team-thread membership. The official-form submission and Discord membership remain outstanding.

Before the final deadline: ensure the public itch.io browser build works from a fresh session; put its link, setup/run instructions, controls and all team details in root README.md; document every external asset and license in root CREDITS.md and on itch.io; disclose every AI tool actually used; preserve honest commit history and respect the code freeze.

Current disclosure: Codex/ChatGPT assisted concept exploration, design review and proposal drafting. OpenAI ImageGen created one pre-jam art-direction concept mockup. No game code or runtime models have been created during this preparation.

## Decisions needed to finalize the proposal

Team name; remaining four members' names, emails and IndieConnect IDs; track; team review of PUNCHLINE; and confirmation of official timestamps. Proposal.pdf remains prominently marked as a draft until these are resolved.
