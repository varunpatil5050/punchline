# PUNCHLINE
## Twist the words. Light the page. Change the ending.

**Proposal draft - 2 October 2026. Team details are incomplete.**

### Game concept

A **3D pop-up comic puzzle platformer** for desktop browsers, designed for a 10-15 minute first playthrough. Comic panels unfold into small playable city dioramas with authored cameras. You play Snap, a background character carrying a flash camera. Printed **BAM!** signs are dormant force emitters: rotate their direction, position yourself or a prop in their marked burst zone, then illuminate the word with a camera flash to make it physically happen. Use the 3D set's depth and height to escape the panels, and redirect the villain's final punch to earn the last frame.

**Art-direction reference:** [AI-generated concept mockup](docs/concepts/punchline-3d-concept.png). This is a design illustration, not a gameplay screenshot or a claim of implemented functionality.

### One action, all three themes

- **Comic:** printed onomatopoeia becomes an interactive 3D object. Folded-paper sets, panel borders, speech bubbles, ink outlines and page transitions shape the presentation.
- **Twist:** rotate a selected word in 90-degree steps to change the direction of its force. The finale turns an apparent finishing blow into the player's escape.
- **Light:** the camera flash activates the selected word. Aiming light identifies the target; the word remains inert until the pulse.

### Rules and player loop

1. Walk to a useful position and aim at a visible sound word within camera range. Solid obstacles block targeting.
2. Twist the word left or right in 90-degree steps within the plane shown by its rotation ring. Some rings turn vertically for upward or sideways launches; others turn horizontally to shove objects across the room. Its world-space arrow and burst-zone outline preview the direction and affected objects.
3. Flash the word. Every movable object in its marked zone receives a fixed, capped impulse in that direction. This includes Snap and crates.
4. Use the launch or shove to reach a ledge, move a crate onto a switch, or open a route to the next panel. Inspect the next challenge and repeat.

Movement crosses the room in 3D with simple authored collision shapes. Fixed room cameras and broad landing areas keep depth and consequences readable. There is no standard jump button: the sound words provide traversal. Failed launches return to the panel checkpoint, and a one-button reset restores the entire panel. Flashes recharge automatically; there is no collectible ammunition or resource grind.

### Intended progression

Eight compact 3D challenges across three comic pages: (1) learn activation and upward launch; (2) rotate a sign to cross a gap; (3) move around an obstruction to light a word; (4) shove a crate across the room onto a switch; (5) use a crate to reach another burst zone; (6) combine two words across broad ledges; (7) reposition a prop while preserving an escape route; (8) redirect the villain's large BAM! using the established rules. Short comic dialogue provides humor between challenges. The ending is playable rather than a separate boss-combat system.

**Controls:** WASD or arrow keys to move across the 3D room; mouse to aim; Q/E to rotate the selected word; left click or Space to flash; R to reset; Escape to pause. The room camera is authored; free camera control is outside scope. Controls remain subject to usability testing.

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

One protagonist; one reusable 3D pop-up city kit; one rotatable sound-effect system; crates, switches, doors and static hazards; eight compact challenges with authored cameras; a beginning, playable finale and credits; checkpoint recovery, reset, pause and audio controls; a public browser build. Visual direction: warm paper, black ink, orange signs and cyan camera light. Stylized models, expressive poses, impact bursts and brief unfolding/page transitions keep the presentation coherent. A short music loop and a small set of purpose-made sounds accompany movement, rotation, flash, impact and victory. Effects remain readable without sound; flash intensity and camera shake can be reduced.

### Implementation and 100-hour delivery plan

Planned engine: Godot 4 with GDScript, Compatibility rendering and a single-threaded web export. The team will create all game code, mechanics and core architecture during the official development window. Five owners cover 3D movement/camera/integration, targeting/force mechanics, level design, 3D art/UI and audio/release testing; names will be assigned by the team. The first eight hours include a representative 3D room tested in the browser.

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

The core promise is rotation plus light activation inside a 3D pop-up comic. Optional extras are cosmetic animation, extra dialogue and replay statistics. Open-world traversal, free camera control, procedural generation, multiplayer, moving enemy AI, a level editor and additional combat systems are outside scope. Simplification will preserve the locked premise and complete playthrough.

The team will test the hosted build on Chromium, Firefox and Safari, observe at least five first-time playthroughs, check recovery from every failure state, and confirm that gameplay, text and controls remain readable at common desktop sizes. Target a typical first completion of 10-15 minutes, with hints and quick recovery to avoid prolonged stalls.

Original, free/open-source, AI-generated or permitted Creative Commons assets only; every external asset will be documented with source and license in root CREDITS.md and on itch.io. Codex/ChatGPT assisted concept exploration and proposal drafting; OpenAI ImageGen produced a pre-jam concept illustration. Any further AI use will be disclosed. Humans own the design, final choices and asset approval. The public repository includes a proper license, proposal.pdf and a README; its itch.io link and setup instructions will be added with the playable build. Registration, team-thread membership and official-form submission must be completed before the applicable deadlines.

**Draft completion requirements:** team name, track, the other four members' names/emails/IDs and team review of the concept. Exact official final deadline still requires confirmation.
