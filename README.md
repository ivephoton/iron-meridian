# Iron Meridian

A vertical scrolling shooter in the Raiden mould. One HTML file, no build step, no dependencies, no asset folder: open `index.html` and fly.

**[Play it here](https://ivephoton.github.io/iron-meridian/)**

---

## Controls

| | Keyboard | Touch / mouse |
|---|---|---|
| Move | Arrow keys or WASD | Drag anywhere on screen |
| Fire | Z, J or Space, held | Fires automatically while you drag |
| Auto-fire | F toggles it | Toggle in the manual |
| Bomb | X or K | The round BOMB button, bottom left |
| Precision | Hold Shift or C for half speed | — |
| Pause | Esc or P opens the manual | The pause button, top right |
| Abandon run | Q, while paused | ABANDON in the manual |
| Sound | M mutes everything · N mutes just the music | Toggles in the manual |

In menus, use the arrow keys, Z or Enter to choose and X or Esc to go back, or just tap.

Only the glowing core takes hits, not the whole ship. Hold precision to see a ring around exactly where it sits.

The BOMB button is always on screen, bottom left, and shows one pip for each bomb you are carrying. Your spare ships sit in the bottom right corner. The middle of the bottom edge carries your weapon and its ten level pips, and your wingmen's gun and their three level pips.

The pause screen is a five-page flight manual (Controls, Weapons, Pods, Pilots, Notes). Turn pages with ← and →, or tap the tabs.

---

## Weapons

Seven weapons, ten power levels each.

| | Weapon | Behaviour | Level 1 → 10 |
|---|---|---|---|
| **V** | Vulcan | Spread cannon | One stream widening to seven across the lane |
| **L** | Lance | Piercing beams that drill through a whole column of hulls | One beam → seven |
| **P** | Plasma | Slow orbs that detonate and splash everything nearby | One small orb → five, splash radius grows throughout |
| **M** | Hornet | Seeking warheads plus a light nose gun | Two warheads per volley → eight, twin nose gun from level 3, triple from level 8 |
| **S** | Arc | Chain lightning with screen-wide reach | Strikes two targets per pulse → eight, and the bolt thickens with every level |
| **F** | Flak | Shells that burst into shrapnel a short way ahead of you | One shell → three, six splinters per burst → sixteen |
| **R** | Ripper | Sawblades that ricochet off the walls and keep cutting | One blade → four, three bounces → eight |

Past level five, each pod adds damage rather than another barrel.

Hornet warheads spread themselves across different targets and prefer ones outside the column in front of you, since the nose gun already covers that.

Arc never misses and never needs aiming, but strikes only a limited number of targets per pulse. Each jump deals less damage than the last, and the pulse splits into two chains from level 3 and three from level 8. The bolt is drawn thicker at every level, from a hairline at level 1 to a fat five-pixel core at level 10, so you can read your power at a glance. It is at its weakest against a lone boss.

Flak shells burst about a third of the way up the screen, or on the first hull they touch. Each splinter then carries around 350 pixels, better than half the height of the playfield, so one burst sweeps a wide arc of sky. Deadly against formations, poor against a single target.

Ripper blades bounce off the side walls and the top of the screen, and cut the same enemy again every third of a second, so a blade loose in a crowded lane does the work of several.

### Pods

Five kinds, all easy to tell apart:

- **Gold round P**: raises the level of the weapon you are flying, up to ten.
- **Coloured capsule with a letter**: switches to that weapon and **keeps the level you already have**, so changing weapons never costs you power. Picking up the letter you are already flying raises the level instead.
- **Dark B token**: a spare bomb, up to ten in hand. Tanks, spinners, gunships and frigates carry them, and so does every boss.
- **Green 1UP token**: a spare ship, up to nine in reserve. The heavier craft carry them, rarely.
- **Wingman token**: puts a drone on each side of you, and upgrades the ones you have. See below.

Pods travel in a straight line and bounce off the edges of the screen, so a pod you miss will swing back past you.

**Every cycling token changes type every five seconds, and disappears only once it has shown every type it carries.** That is 35 seconds for a weapon capsule, which runs V → L → P → M → S → F → R, and 15 seconds for a wingman token, which runs through its three guns. A gold P, bomb or ship token lasts 35 seconds too. All of them blink for their last three seconds, and the ring around a cycling token shows how long the current type has left. Leave a letter you don't want alone and it will become one you do.

Every wave sends at least one **pod carrier**, a slow rotor craft with a colour-cycling cargo light, which always drops a pod. Boss waves send one too. Other enemies drop pods occasionally, and so does wiping out a whole formation.

Bomb and ship tokens drop on their own rolls, so a frigate can leave a weapon pod, a bomb and a spare ship behind at once:

| Enemy | Bomb token | Spare ship |
|---|---|---|
| Tank | 5% | 1% |
| Spinner | 12% | 1.5% |
| Pod carrier | — | 4% |
| Gunship | 30% | 3% |
| Frigate | 55% | 7% |

Those chances are scaled by the difficulty's pod drop rate, so Cadet sees more and Meridian fewer.

---

## Wingmen (僚机)

A wingman token puts a drone on each side of your ship. They trail the ship, fire whenever you do, and cannot be hit.

Three levels:

| Level | What you get |
|---|---|
| 1 | One drone on each side |
| 2 | Half again the rate of fire |
| 3 | A second drone on each side, four in all |

Three guns, and the token cycles through them every five seconds, exactly like a weapon capsule:

| | Gun | Behaviour |
|---|---|---|
| **I** | Needle | Straight pellets, fast and steady |
| **X** | Spray | An angled fan either side, for sweeping a lane |
| **H** | Homer | Slow seekers that pick their own targets |

Picking up the letter your wingmen already carry raises their level; a different letter changes their gun and keeps the level. Losing a ship costs one wingman level.

---

## Pilots

Five, with real trade-offs rather than palette swaps.

| Pilot | Character | Speed | Ships | Bombs | Core |
|---|---|---|---|---|---|
| **Falcon** | Balanced. No weaknesses, no gimmicks | 300 | ±0 | 3 | Standard |
| **Bolt** | Fastest ship and smallest hitbox, one fewer life | 372 | −1 | 3 | Small |
| **Aegis** | Spare ship and spare bomb, sluggish turns | 262 | +1 | 4 | Standard |
| **Havoc** | 65% more damage at half the fire rate | 292 | ±0 | 3 | Large |
| **Nyx** | Enormous fire rate (×2.5), feather-light shots (×0.36), two extra bombs | 300 | ±0 | 5 | Standard |

Speed is in pixels per second on the 480×720 playfield. Ships are added to or taken from the difficulty's starting count, and you always get at least one. Aegis carries momentum through every turn, so it drifts before it changes direction.

---

## Bombs and losing a ship

A bomb erases every enemy bullet on screen (10 points each), damages everything for about a second and a half, and makes you untouchable for nearly three seconds. You can carry ten.

Losing a ship costs two weapon levels and one wingman level, and the lost power drops as a gold P where you went down, so you can win some of it back. The next ship flies in with about three seconds of invulnerability and your bombs refilled to your pilot's starting count, or left as they are if you had collected more than that.

---

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

---

## Waves

Two constants set the overall pitch of the game: `ENEMY_HP_SCALE` (`0.385`) scales the health of everything you shoot at, and `ENEMY_BULLET_SCALE` (`0.805`) scales the speed of every enemy and boss bullet. Raise either to make the game harder without touching anything else.

Waves escalate endlessly. Each wave adds 8.5% of an enemy's base health to its hull. As the waves climb, enemies fire up to twice as often, shoot bullets up to 35% faster and fly in formations up to 50% larger, reaching those limits around wave 20. New enemy types join as you go:

| From wave | Enemies |
|---|---|
| 1 | Darts in V, swoop and sweep formations · hovering drones · pod carriers |
| 2 | Ground tanks with tracking turrets · fast dart columns aimed down your lane |
| 3 | Spinners that lay spiral bullet streams · heavy gunships |
| 4 | Kamikazes that home in on you |
| 8 | Frigates |

A fast dart column is announced by a flashing red line down the lane it is about to fly through.

The ground changes after every boss, from Coastline to Foundry, Dune Sea and Night Grid, then round again.

---

## Bosses

Every fifth wave is a boss, announced by a WARNING banner.

| Wave | Boss | Attack patterns |
|---|---|---|
| 5 | **Warden** | Wing Batteries · Core Rings · Sweep Curtain |
| 10 | **Hydra** | Triple Heads · Spores · Brood |
| 15 | **Seraph** | Twin Spirals · Falling Walls · Feather Volleys |
| 20 | **Leviathan** | Rain Lanes · Bloom Orbs · Rose |

Each boss cycles through its three patterns, about eight seconds each with a short breather between, and each pattern's name flashes up as it begins. As a boss's health falls it fires faster, adds bullets and moves more aggressively.

After wave 20 the bosses come round again, each one tougher than the last: Warden returns at wave 25 with twice its original health, and at wave 45 with three times. Returning bosses also fire more often and shoot faster bullets. A destroyed boss is worth 20,000 points times how many bosses you have met, and drops a gold P, a weapon capsule, a bomb token and a wingman token (plus an extra P on Cadet).

---

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

- **Chain:** each kill within 1.6 seconds of the last extends your chain. Every five kills in a chain adds ×1 to the multiplier, up to ×8, and every kill is worth its points times the multiplier. Losing a ship resets it.
- **Formation bonus:** destroy every ship in a formation of four or more, with none escaping, for 200 points per ship, times your multiplier.
- **Pickups:** any pod is worth 250 points. A power-up at full power is worth 5,000 more; a bomb token with ten bombs in hand is worth 2,000 more, and a ship or wingman token you cannot use is worth 3,000 more.
- **Bombs:** every enemy bullet a bomb erases is worth 10 points.

The best score lasts as long as the tab does. Nothing is written to disk.

---

## Sound

Both the effects and the four music tracks are synthesised at runtime with the Web Audio API; there are no audio files. A step sequencer schedules notes slightly ahead of the audio clock so timing doesn't drift with the frame rate, and the track follows the game: something sparse in the menus, driving in combat, more dissonant for bosses, and a slow fall on death.

Browsers only allow sound after you interact with the page, so the music starts with your first key press or tap.

Audio suspends whenever the page is backgrounded, the screen locks, or the tab closes. This matters on iOS, where Safari will otherwise keep a running audio context alive behind a home-screen swipe. Returning to the page resumes sound and leaves the game paused on the manual.

---

## Running it

No tooling required. Play it online at the link above, or clone the repository and open the file:

```
git clone https://github.com/ivephoton/iron-meridian.git
cd iron-meridian
open index.html          # macOS
start index.html         # Windows
xdg-open index.html      # Linux
```

Double-clicking `index.html` works too. It makes no network requests, so it runs offline.

### Putting it on GitHub

The repository only needs two files at its root: `index.html` and this `README.md`.

1. On GitHub, create a new repository named `iron-meridian`.
2. Choose **Add file → Upload files**, drag in `index.html` and `README.md`, and commit.
3. To publish it as a playable page, go to **Settings → Pages**, set the source to **Deploy from a branch**, the branch to `main` and the folder to `/ (root)`, then save.

After a minute or two the game is live at `https://<your-username>.github.io/iron-meridian/`. The file must be named `index.html` for Pages to serve it at the repository root.

---

## Tuning

The balance lives in plain constants near the top of `index.html`:

| Constant | What it controls |
|---|---|
| `ENEMY_HP_SCALE` | Health of every enemy and boss, on every wave and difficulty (currently `0.385`) |
| `ENEMY_BULLET_SCALE` | Speed of every enemy and boss bullet, on every wave and difficulty (currently `0.805`) |
| `MAX_LEVEL` | Power levels per weapon (currently `10`) |
| `WING_MAX` | Wingman levels (currently `3`) |
| `LV` | The per-level tables: streams, beams, orbs, warheads, strikes, shells, splinters, blades and bounces |
| `WING_TYPES`, `WING_RATE`, `WING_DMG` | The three wingman guns, and what each level adds |
| `DIFFS` | The three difficulty settings in the table above |
| `PILOTS` | Speed, handling, core size, ships, bombs, damage and fire rate per pilot |
| `ETYPES` | Base health, size, score, pod chance, bomb-token chance and spare-ship chance for each enemy |
| `BOSSES` | Base health, hitboxes and pattern names for each boss |
| `BASE_BOMBS` | Bombs every pilot starts with, before pilot bonuses (currently `3`) |
| `CHAIN_WINDOW` | Seconds you have between kills to keep a chain alive (currently `1.6`) |
| `POD_CYCLE` | Seconds each type shows on a cycling token (currently `5`) |
| `POD_LAPS` | How many times a token shows every type before it disappears (currently `1`) |
| `POD_SPEED` | How fast pods drift, in pixels per second |
| `BOMB_DURATION`, `BOMB_DPS`, `BOMB_INVULN` | How long a bomb burns, how hard it hits, and how long it protects you |
| `RESPAWN_INVULN` | Seconds of invulnerability for a new ship |
| `MAX_MULTIPLIER` | The chain multiplier cap (currently `8`) |
| `MAX_BOMBS` | Most bombs you can carry (currently `10`) |
| `MAX_SHIPS` | Most ships you can hold in reserve (currently `9`) |
| `GROUND_SPEED` | How fast the ground scrolls |

A cycling token's lifetime is `POD_LAPS × (number of types) × POD_CYCLE` seconds, so lowering `POD_CYCLE` makes tokens cycle faster and vanish sooner.

---

## Built with

Plain JavaScript and a 480×720 canvas, scaled to fit the window and sharpened for high-density screens. Ships, enemies and bosses are drawn as vector paths rather than sprites, and the four ground regions are generated once into seamless tiles. Headings and the HUD use a 5×7 dot-matrix typeface drawn in code; the flight manual's body text uses the system's Georgia or Times. Everything, including game, art and music, lives in `index.html`, so the page works offline and nothing can 404.

The script inside `index.html` is laid out top to bottom in labelled sections:

| Section | Contents |
|---|---|
| Playfield, Tuning, Palette | Every constant listed above |
| Maths, Canvas and scaling, Input | Helpers, window fitting, keyboard and pointer handling |
| Sound, Music | Synthesised effects and the step-sequenced soundtrack |
| Dot-matrix type, Sprites, Vector ships | Text rendering, bullet and glow sprites, the five player ships |
| Ground | The four scrolling regions and clouds |
| World state, Particles, Player, Weapons, Wingmen, Enemies, Pods, Bomb, Collisions | Gameplay |
| Enemy art, Bosses, Boss art | Enemy drawing, boss attack patterns and boss drawing |
| Waves, Runs | The wave director, starting and ending a run |
| Interface, Menu input, Title, Difficulty, Pilot select, HUD, Flight manual, Game over | Every screen |
| Main loop, Boot | The frame loop, pausing when backgrounded, start-up |

---

## Licence

MIT.
