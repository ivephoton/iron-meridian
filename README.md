# Iron Meridian

A vertical scrolling shooter in the Raiden mould. One HTML file, no build step, no dependencies, no asset folder: open `index.html` and fly.

**[Play it here](https://ivephoton.github.io/iron-meridian/)**

## Controls

| | Keyboard | Touch / mouse |
|---|---|---|
| Move | Arrow keys or WASD | Drag anywhere on screen |
| Fire | Hold Z, J or Space | Fires automatically while you drag |
| Auto-fire | F to toggle | Toggle in the manual |
| Bomb | X or K | Round BOMB button, bottom right (touch screens only) |
| Precision (half speed) | Hold Shift or C | — |
| Pause | Esc or P | Pause button, top right |
| Abandon run | Q while paused | ABANDON in the manual |
| Sound | M mutes everything, N mutes only the music | Toggles in the manual |

In menus, move with the arrow keys, choose with Z or Enter, and go back with X or Esc. Or tap: on the difficulty and pilot screens, the first tap highlights a card and a second tap chooses it.

Only the glowing core of your ship can be hit. Hold precision to show a ring around it.

Spare ships and bombs sit in the bottom left corner, one small ship per spare and one gold pip per bomb, with your weapon and its level in the middle. On touch screens a round BOMB button sits just above the bottom right corner and shows how many bombs you have left.

Pausing opens a four-page flight manual (Controls, Weapons, Pilots, Field Notes). Turn pages with ← and → or tap the tabs.

## Weapons

Five weapons, five power levels each.

| | Weapon | Behaviour | Level 1 → 5 |
|---|---|---|---|
| **V** | Vulcan | Spread cannon | One stream → five, fanning across the lane |
| **L** | Lance | Piercing beams that drill through every hull in a column | One beam → five |
| **P** | Plasma | Slow orbs that detonate and splash everything nearby | One small orb → three, with a growing splash radius |
| **M** | Hornet | Seeking warheads plus a light nose gun | Two warheads per volley → six, twin nose gun from level 3 |
| **S** | Arc | Chain lightning with screen-wide reach | Strikes two targets per pulse → six |

Hornet warheads spread across different targets and favour those outside the column in front of you, which the nose gun already covers.

Arc never misses and needs no aiming, but each pulse strikes a limited number of targets and every jump deals less damage than the last. From level 3 the pulse splits into two chains. It is weakest against a lone boss.

### Pods

There are two kinds:

- **Round gold P**: raises your current weapon's level.
- **Coloured capsule with a letter**: switches to that weapon at your current level. If it's the weapon you already have, it raises the level instead.

Pods travel in straight lines and bounce off the screen edges, so one you miss will usually swing back past you. **Each pod survives three bounces, blinks after its third, and pops on its fourth**, which typically takes 15 to 35 seconds. Gold Ps and capsules follow the same rule, and neither has a time limit.

Every ten seconds a capsule switches to the next weapon (V → L → P → M → S), and the ring around it shows how long is left. If you don't want the letter on offer, wait for the next one, though most capsules pop after showing two to four letters.

Every wave, boss waves included, sends at least one **pod carrier**: a slow rotor craft with a colour-cycling cargo light that always drops a pod. Other enemies occasionally drop pods, and wiping out a whole formation sometimes does too.

## Pilots

Five, with real trade-offs rather than palette swaps.

| Pilot | Character | Speed | Ships | Bombs | Core |
|---|---|---|---|---|---|
| **Falcon** | Balanced: no weaknesses, no gimmicks | 300 | ±0 | 3 | Standard |
| **Bolt** | Fastest ship and smallest hitbox, but one fewer ship | 372 | −1 | 3 | Small |
| **Aegis** | An extra ship and bomb, but sluggish turns | 262 | +1 | 4 | Standard |
| **Havoc** | 65% more damage at half the fire rate | 292 | ±0 | 3 | Large |
| **Nyx** | Enormous fire rate (×2.5), feather-light shots (×0.36), two extra bombs | 300 | ±0 | 5 | Standard |

Speed is in pixels per second on the 480×720 playfield. Ships adjust the difficulty's starting count, with a minimum of one. Aegis carries momentum through every turn, so it drifts before changing direction.

## Bombs and losing a ship

A bomb burns for about a second and a half, erasing every enemy bullet on screen (10 points each) and damaging everything for as long as it lasts. It also makes you untouchable for nearly three seconds.

Losing a ship costs up to two weapon levels (never below level 1). If you lose any, a gold P drops where you went down so you can win one back. Your next ship flies in with about three seconds of invulnerability and bombs refilled to your pilot's starting count.

## Difficulty

| | Cadet | Regular | Meridian |
|---|---|---|---|
| Starting ships | 5 | 3 | 2 |
| Enemy bullet speed | ×0.72 | ×1 | ×1.28 |
| Time between enemy shots | ×1.5 | ×1 | ×0.68 |
| Enemy hull strength | ×0.72 | ×1 | ×1.35 |
| Formation size | ×0.75 | ×1 | ×1.32 |
| Pod drop rate | ×1.45 | ×1 | ×0.72 |
| Boss health | ×0.68 | ×1 | ×1.45 |

## Waves

Waves escalate endlessly, and each one adds 8.5% of an enemy's base health to its hull. Fire rate, bullet speed and formation size climb too, reaching their limits around wave 20: double the fire rate, 35% faster bullets and 50% larger formations. New enemy types join along the way:

| From wave | Enemies |
|---|---|
| 1 | Darts in V, swoop and sweep formations · hovering drones · pod carriers |
| 2 | Ground tanks with tracking turrets · fast dart columns aimed down your lane |
| 3 | Spinners that lay spiral bullet streams · heavy gunships |
| 4 | Kamikazes that home in on you |
| 8 | Frigates |

A flashing red line marks the lane a fast dart column is about to fly down.

The ground changes after every boss: Coastline, Foundry, Dune Sea, Night Grid, then round again.

## Bosses

Every fifth wave is a boss wave, announced by a WARNING banner.

| Wave | Boss | Attack patterns |
|---|---|---|
| 5 | **Warden** | Wing Batteries · Core Rings · Sweep Curtain |
| 10 | **Hydra** | Triple Heads · Spores · Brood |
| 15 | **Seraph** | Twin Spirals · Falling Walls · Feather Volleys |
| 20 | **Leviathan** | Rain Lanes · Bloom Orbs · Rose |

Each boss cycles through its three patterns for about eight seconds apiece, with a short breather between, and each pattern's name flashes up as it begins. As its health falls, a boss fires faster, adds bullets and moves more aggressively.

After wave 20 the bosses come round again, tougher each time: Warden returns at wave 25 with twice its original health and at wave 45 with three times. Returning bosses also fire more often and shoot faster bullets. A destroyed boss drops a gold P and a weapon capsule, plus an extra P on Cadet.

## Scoring

| Enemy | Points |
|---|---|
| Dart | 100 |
| Kamikaze | 150 |
| Drone | 300 |
| Tank | 400 |
| Spinner | 600 |
| Pod carrier | 1,000 |
| Gunship | 1,500 |
| Frigate | 3,000 |
| Boss | 20,000 × the number of bosses you've met |

- **Chain:** each kill within 1.6 seconds of the last extends your chain. Every five kills in a chain adds ×1 to your multiplier, up to ×8, and each kill scores its points times the multiplier. Losing a ship resets the chain.
- **Formation bonus:** destroy every ship in a formation of four or more, letting none escape, for 200 points per ship times your multiplier.
- **Pickups:** every pod is worth 250 points, and a power-up collected at full power is worth 5,000 more.
- **Bombs:** every enemy bullet a bomb erases is worth 10 points.

Your best score is kept until you close the tab. Nothing is saved to disk.

## Sound

The sound effects and all four music tracks are synthesised at runtime with the Web Audio API; there are no audio files. A step sequencer schedules notes slightly ahead of the audio clock so timing doesn't drift with the frame rate. The music follows the game: sparse in the menus, driving in combat, more dissonant for bosses, and a slow fall on death.

Browsers only allow sound after you interact with the page, so the music starts with your first key press or tap.

Audio suspends whenever the page is backgrounded, the screen locks or the tab closes. This matters on iOS, where Safari would otherwise keep audio running after you swipe to the home screen. When you come back, sound resumes and the game waits, paused on the manual.

## Running it

Play it online at the link above, or clone the repository and open the file:

```
git clone https://github.com/ivephoton/iron-meridian.git
cd iron-meridian
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

Double-clicking `index.html` works too. The game makes no network requests, so it runs offline.

### Putting it on GitHub

The repository only needs two files at its root: `index.html` and this `README.md`.

1. On GitHub, create a new repository named `iron-meridian`.
2. Choose **Add file → Upload files**, drag in `index.html` and `README.md`, and commit.
3. To publish it as a playable page, go to **Settings → Pages**, set the source to **Deploy from a branch**, the branch to `main` and the folder to `/ (root)`, then save.

After a minute or two the game is live at `https://<your-username>.github.io/iron-meridian/`. Pages only serves it at that address if the file is named `index.html`.

## Tuning

The balance lives in plain constants near the top of `index.html`:

| Constant | What it controls |
|---|---|
| `ENEMY_HP_SCALE` | Scales the health of every enemy and boss, on every wave and difficulty (currently `0.7`) |
| `DIFFS` | The three difficulty settings (see Difficulty) |
| `PILOTS` | Speed, handling, core size, ships, bombs, damage and fire rate per pilot |
| `ETYPES` | Base health, size, score and drop chance for each enemy |
| `BOSSES` | Base health, hitboxes and pattern names for each boss |
| `BASE_BOMBS` | Bombs every pilot starts with, before pilot bonuses (currently `3`) |
| `CHAIN_WINDOW` | Seconds you have between kills to keep a chain alive (currently `1.6`) |
| `POD_CYCLE` | Seconds each weapon letter shows on a capsule (currently `10`) |
| `POD_BOUNCES` | How many edge bounces a pod survives before it pops on the next one (currently `3`) |
| `POD_SPEED` | How fast pods drift, in pixels per second |
| `BOMB_DURATION`, `BOMB_DPS`, `BOMB_INVULN` | How long a bomb burns, how hard it hits, and how long it protects you |
| `RESPAWN_INVULN` | Seconds of invulnerability for a new ship |
| `MAX_MULTIPLIER` | The chain multiplier cap (currently `8`) |
| `GROUND_SPEED` | How fast the ground scrolls |

A pod's lifetime is set by bounces, not time: raising `POD_BOUNCES` or lowering `POD_SPEED` keeps pods on screen longer, while `POD_CYCLE` only changes how quickly a capsule's letter turns over.

## Built with

Plain JavaScript and a 480×720 canvas, scaled to fit the window and sharpened for high-density screens. Ships, enemies and bosses are drawn as vector paths rather than sprites, and the four ground regions are generated once into seamless tiles. Headings and the HUD use a 5×7 dot-matrix typeface drawn in code; the flight manual's body text uses the system's Georgia or Times. Game, art and music all live in `index.html`, so the page works offline and nothing can 404.

The script in `index.html` runs top to bottom through these labelled sections:

| Section | Contents |
|---|---|
| Playfield, Tuning, Palette | The constants listed under Tuning |
| Maths, Canvas and scaling, Input | Helpers, window fitting, keyboard and pointer handling |
| Sound, Music | Synthesised effects and the step-sequenced soundtrack |
| Dot-matrix type, Sprites, Vector ships | Text rendering, bullet and glow sprites, the five player ships |
| Ground | The four scrolling regions and clouds |
| World state, Particles, Player, Weapons, Enemies, Pods, Bomb, Collisions with the player | Gameplay |
| Enemy art, Bosses, Boss art | Enemy drawing, boss attack patterns and boss drawing |
| Waves, Runs | The wave director, starting and ending a run |
| Interface, Menu input, Shared drawing, Title, Difficulty, Pilot select, HUD, Flight manual, Game over | Every screen |
| Main loop, Boot | The frame loop, pausing when backgrounded, start-up |

## Licence

MIT.
