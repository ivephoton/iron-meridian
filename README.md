# Iron Meridian

A vertical scrolling shooter in the Raiden mould. One HTML file, no build step, no dependencies, no asset folder: open `index.html` and fly.

**[Play it here](https://ivephoton.github.io/iron-meridian/)**

---

## Controls

| | Keyboard | Touch / mouse |
|---|---|---|
| Move | Arrow keys or WASD | Drag anywhere on screen |
| Fire | Z, J or Space, held | Fires automatically on touch |
| Auto-fire | F toggles it | Toggle in the manual |
| Bomb | X or K | The round BOMB button, bottom right |
| Precision | Hold Shift or C for half speed | — |
| Pause | Esc or P opens the manual | The pause button, top right |
| Abandon run | Q, while paused | ABANDON in the manual |
| Sound | M mutes everything · N mutes just the music | Toggles in the manual |

In menus, use the arrow keys, Z or Enter to choose and X or Esc to go back, or just tap.

Only the glowing core takes hits, not the whole ship. Hold precision to see a ring around exactly where it sits.

The pause screen is a four-page flight manual (Controls, Weapons, Pilots, Field Notes). Turn pages with ← and →.

---

## Weapons

Five weapons, five power levels each.

| | Weapon | Behaviour | Level 1 → 5 |
|---|---|---|---|
| **V** | Vulcan | Spread cannon | One stream widening to five across the lane |
| **L** | Lance | Piercing beams that drill through a whole column of hulls | One beam → five |
| **P** | Plasma | Slow orbs that detonate and splash everything nearby | One small orb → three, splash radius grows |
| **M** | Hornet | Seeking warheads plus a light nose gun | Two warheads per volley → six, twin nose gun from level 3 |
| **S** | Arc | Chain lightning with screen-wide reach | Strikes two targets per pulse → six |

Hornet warheads spread themselves across different targets and prefer ones outside the column in front of you, since the nose gun already covers that.

Arc never misses and never needs aiming, but strikes only a limited number of targets per pulse. Each jump deals less damage than the last, and from level 3 the pulse splits into two chains. It is at its weakest against a lone boss.

### Pods

There are two kinds, and they are easy to tell apart:

- **Gold round P**: raises your current weapon's level.
- **Coloured capsule with a letter**: switches to that weapon and keeps your level. Picking up the letter you already have raises the level instead.

Pods travel in a straight line and bounce off the edges of the screen. Each survives three bounces, blinks on its last, and pops on the fourth, so a pod you miss will usually swing back past you. Weapon capsules cycle to the next weapon (V → L → P → M → S) every ten seconds, and the ring around a capsule shows how long is left. Leave a letter you don't want alone and it will become one you do.

Every wave sends at least one **pod carrier**, a slow rotor craft with a colour-cycling cargo light, which always drops a pod. Other enemies drop pods occasionally, and so does wiping out a whole formation.

---

## Pilots

Five, with real trade-offs rather than palette swaps.

| Pilot | Character | Ships | Bombs | Core |
|---|---|---|---|---|
| **Falcon** | Balanced. No weaknesses, no gimmicks | ±0 | 3 | Standard |
| **Bolt** | Fastest ship and smallest hitbox, one fewer life | −1 | 3 | Small |
| **Aegis** | Spare ship and spare bomb, sluggish turns | +1 | 4 | Standard |
| **Havoc** | 65% more damage at half the fire rate | ±0 | 3 | Large |
| **Nyx** | Enormous fire rate, feather-light shots, two extra bombs | ±0 | 5 | Standard |

Ships are added to or taken from the difficulty's starting count, and you always get at least one. Aegis carries momentum through every turn, so it drifts before it changes direction.

---

## Bombs and losing a ship

A bomb erases every enemy bullet on screen (10 points each), damages everything for about a second and a half, and makes you untouchable for nearly three seconds.

Losing a ship costs two weapon levels, and the lost power drops as a gold P where you went down, so you can win some of it back. The next ship flies in with about three seconds of invulnerability and your bombs refilled to your pilot's starting count.

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

Waves escalate endlessly. Each wave adds 8.5% of an enemy's base health to its hull, and as the waves climb enemies fire up to twice as often, shoot up to 35% faster bullets and fly in formations up to 50% larger. New enemy types join as you go:

| From wave | Enemies |
|---|---|
| 1 | Darts in V, swoop and sweep formations · hovering drones · pod carriers |
| 2 | Ground tanks with tracking turrets · fast dart columns aimed down your lane |
| 3 | Spinners that lay spiral bullet streams · heavy gunships |
| 4 | Kamikazes that home in on you |
| 8 | Frigates |

The ground changes after every boss, from Coastline to Foundry, Dune Sea and Night Grid, then round again.

---

## Bosses

Every fifth wave is a boss.

| Wave | Boss | Attack patterns |
|---|---|---|
| 5 | **Warden** | Wing Batteries · Core Rings · Sweep Curtain |
| 10 | **Hydra** | Triple Heads · Spores · Brood |
| 15 | **Seraph** | Twin Spirals · Falling Walls · Feather Volleys |
| 20 | **Leviathan** | Rain Lanes · Bloom Orbs · Rose |

Each boss cycles through its three patterns, and each pattern's name flashes up as it begins. As a boss's health falls it fires faster, adds bullets and moves more aggressively.

After wave 20 the bosses come round again, each one tougher than the last: Warden returns at wave 25 with twice its original health. A destroyed boss is worth 20,000 points times how many bosses you have met, and drops a gold P and a weapon capsule (plus an extra P on Cadet).

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

- **Chain:** each kill within 1.6 seconds of the last extends your chain. Every five kills in a chain adds ×1 to the multiplier, up to ×8. Losing a ship resets it.
- **Formation bonus:** destroy every ship in a formation of four or more, with none escaping, for 200 points per ship, times your multiplier.
- **Pickups:** any pod is worth 250 points, and a power-up at full power is worth 5,000 more.

The best score lasts as long as the tab does. Nothing is written to disk.

---

## Sound

Both the effects and the four music tracks are synthesised at runtime with the Web Audio API; there are no audio files. A step sequencer schedules notes slightly ahead of the audio clock so timing doesn't drift with the frame rate, and the track follows the game: something sparse in the menus, driving in combat, more dissonant for bosses, and a slow fall on death.

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

To publish your own copy: **Settings → Pages**, source **Deploy from a branch**, branch `main`, folder `/ (root)`. The file must be named `index.html` for Pages to serve it at the repository root.

---

## Tuning

The balance lives in a handful of plain constants in `index.html`:

| Constant | What it controls |
|---|---|
| `ENEMY_HP_SCALE` | Health of every enemy and boss, on every wave and difficulty (currently `0.7`) |
| `DIFFS` | The three difficulty settings in the table above |
| `PILOTS` | Speed, handling, core size, ships, bombs, damage and fire rate per pilot |
| `ETYPES` | Base health, size, score and drop chance for each enemy |
| `BOSSES` | Base health, hitboxes and pattern names for each boss |
| `BASE_BOMBS` | Bombs every pilot starts with, before pilot bonuses |
| `CHAIN_WINDOW` | Seconds you have between kills to keep a chain alive |

---

## Built with

Plain JavaScript and a 480×720 canvas, scaled to fit the window and sharpened for high-density screens. Ships, enemies and bosses are drawn as vector paths rather than sprites, and the four ground regions are generated once into seamless tiles. Everything, including game, art and music, lives in `index.html`, so the page works offline and nothing can 404.

---

## Licence

MIT.
