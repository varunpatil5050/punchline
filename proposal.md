# PUNCHLINE
## Twist the words. Light the page. Change the ending.

**Proposal draft - 2 October 2026. Team details are incomplete.**

### Game concept

A 2D comic puzzle platformer for desktop browsers, designed for a 10-15 minute first playthrough. You play Snap, a background character carrying a flash camera. Printed **BAM!** effects are dormant force emitters: rotate their direction, position yourself or a prop in their marked burst zone, then illuminate the word with a camera flash to make it physically happen. Escape the comic's panels and redirect the villain's final punch to earn the last frame.

### One action, all three themes

- **Comic:** printed onomatopoeia becomes an interactive object. Panel borders, speech bubbles, ink outlines and page transitions also shape the presentation.
- **Twist:** rotate a selected word in 90-degree steps to change the direction of its force. The finale turns an apparent finishing blow into the player's escape.
- **Light:** the camera flash activates the selected word. Aiming light identifies the target; the word remains inert until the pulse.

### Rules and player loop

1. Walk to a useful position and aim at a visible sound word within camera range. Solid obstacles block targeting.
2. Twist the word left or right. Its arrow and burst-zone outline preview the direction and affected objects.
3. Flash the word. Every movable object in its marked zone receives a fixed, capped impulse in that direction. This includes Snap and crates.
4. Use the launch or shove to reach a ledge, move a crate onto a switch, or open a route to the next panel. Inspect the next challenge and repeat.

Movement uses simple authored collision shapes; challenges depend on positioning and readable cause and effect. There is no standard jump button: the sound words provide traversal. Failed launches return to the panel checkpoint, and a one-button reset restores the entire panel. Flashes recharge automatically; there is no collectible ammunition or resource grind.

### Intended progression

Eight compact challenges across three comic pages: (1) learn activation and upward launch; (2) rotate a word to cross a gap; (3) light a word from a safe angle; (4) shove a crate onto a switch; (5) use a crate to reach another burst zone; (6) combine two words in sequence; (7) reposition a prop while preserving an escape route; (8) redirect the villain's large BAM! using the established rules. Short comic dialogue provides humor between challenges. The ending is playable rather than a separate boss-combat system.

**Controls:** A/D or left/right arrows to move; mouse to aim; Q/E to rotate the selected word; left click or Space to flash; R to reset; Escape to pause. Controls remain subject to usability testing.

---

### Team

**Team name:** pending. **Track:** pending confirmation. **Public GitHub repository:** https://github.com/varunpatil5050/punchline

| Member | Email | IndieConnect ID |
| --- | --- | --- |
| Varun Patil | varun.patil@students.iiit.ac.in | @varunp685 |
| Teammate 2 - pending | pending | pending |
| Teammate 3 - pending | pending | pending |
| Teammate 4 - pending | pending | pending |
| Teammate 5 - pending | pending | pending |

### Committed scope and presentation

One protagonist; one rotatable sound-word force system; crates, switches, doors and static hazards; eight compact challenges; a beginning, playable finale and credits; checkpoint recovery, reset, pause and audio controls; a public browser build. Visual direction: warm paper, black ink, orange sound words and cyan camera light. Reusable character poses, brief squash/stretch, printed impact bursts and page transitions keep the presentation coherent. A short music loop and a small set of purpose-made sounds accompany movement, rotation, flash, impact and victory. Effects remain readable without sound; flash intensity and camera shake can be reduced.

### Implementation and 100-hour delivery plan

Planned engine: Godot 4 with GDScript, Compatibility rendering and a single-threaded web export. The team will create all game code, mechanics and core architecture during the official development window. Five owners cover integration/game feel, the camera/force system, level design, art/UI and audio/release testing; names will be assigned by the team.

| Elapsed time from official Hour 0 | Delivery gate |
| --- | --- |
| 0-8 hours | One complete challenge with launch, rotation, flash, reset and a tested web export. |
| 8-24 hours | Complete core loop and shared level components; early hosted build. |
| 24-48 hours | Eight challenges assembled; assets and sound integrated. |
| 48-64 hours | Full beginning-to-credits run, including the finale. |
| 64-82 hours | Uncoached first-time playtests; tune clarity, difficulty and 10-15 minute duration. |
| 82-92 hours | Feature freeze; browser and machine testing; fix completion blockers. |
| 92-100 hours | Final release, documentation and submission buffer. |

### Boundaries, validation and disclosures

The core promise is rotation plus light activation inside a comic. Optional extras are cosmetic animation, extra dialogue and replay statistics. Procedural generation, multiplayer, moving enemy AI, a level editor and additional combat systems are outside scope. Simplification will preserve the locked premise and complete playthrough.

The team will test the hosted build on Chromium, Firefox and Safari, observe at least five first-time playthroughs, check recovery from every failure state, and confirm that gameplay, text and controls remain readable at common desktop sizes. Target a typical first completion of 10-15 minutes, with hints and quick recovery to avoid prolonged stalls.

Original, free/open-source, AI-generated or permitted Creative Commons assets only; every external asset will be documented with source and license in root CREDITS.md and on itch.io. Codex/ChatGPT assisted concept exploration and proposal drafting; any further AI use will be disclosed. Humans own the design, final choices and asset approval. The public repository will include a proper license, proposal.pdf and a README with the itch.io link, setup, controls and team details. Registration, team-thread membership and official-form submission must be completed before the applicable deadlines.

**Draft completion requirements:** team name, track, the other four members' names/emails/IDs and team review of the concept. Exact official final deadline still requires confirmation.
