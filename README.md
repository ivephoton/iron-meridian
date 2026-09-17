# Iron Meridian

A vertical scrolling shooter in the Raiden mould. One HTML file, no build step, no dependencies, no asset folder — open `index.html` and fly.

**[Play it here](https://ivephoton.github.io/iron-meridian/)**

---

## Controls

| | |
|---|---|
| Move | Arrow keys or WASD, or drag anywhere on screen |
| Fire | Z, J or space — hold to keep firing |
| Auto-fire | F toggles it on and off. Touch always auto-fires |
| Bomb | X or K, or the round BOMB button at the bottom right |
| Precision | Hold shift or C to halve your speed for tight gaps |
| Pause | Esc or P — opens the manual. Q abandons the run |
| Sound | M silences everything · N turns just the music off |

Only the glowing core takes hits, not the whole ship. Hold precision to see exactly where it sits.

---

## Weapons

Five weapons, five power levels each. A lettered pod swaps your weapon; picking up your current letter again, or a gold **P**, raises its level toward 5.

| | Weapon | Behaviour |
|---|---|---|
| **V** | Vulcan | Spread cannon, widening from one shot to five across the lane |
| **L** | Lance | Piercing beams that drill through a whole column of hulls |
| **P** | Plasma | Slow orbs that detonate, splashing damage into everything nearby |
| **M** | Hornet | Seeking warheads plus a light nose gun — hits what you aren't aiming at |
| **S** | Arc | Chain lightning with screen-wide reach; picks its own targets and jumps between them |

Arc never misses and never needs aiming, but strikes only a limited number of targets per pulse — two at level 1, six at level 5 — with damage falling off along each chain.

### Pods

Dropped pods travel in a straight line and bounce off the edges of the screen. Each survives three bounces, blinks on its last, and pops on the fourth, so a power-up you miss will usually swing back past you. Weapon pods also cycle to a different weapon every ten seconds, which means a letter you don't want will eventually become one you do if you leave it alone.

---

## Pilots

Five, with real trade-offs rather than palette swaps.

| Pilot | Character |
|---|---|
| **Falcon** | Balanced. No weaknesses, no gimmicks |
| **Bolt** | Fastest ship and smallest hitbox, one fewer life |
| **Aegis** | Spare ship and spare bomb, sluggish turns |
| **Havoc** | 65% more damage at half the fire rate |
| **Nyx** | Enormous fire rate, feather-light shots, two extra bombs |

---

## Difficulty

**Cadet**, **Regular** and **Meridian** change bullet speed, enemy fire intervals, hull strength, formation density, drop rate, boss health, and how many ships you start with — five, three or two.

---

## Structure

Waves escalate endlessly, with a boss every fifth wave drawn from four designs. Each boss cycles three attack patterns and grows more aggressive as its health falls. Killing enemies in quick succession builds a chain multiplier.

---

## Sound

Both the effects and the four music tracks are synthesised at runtime with the Web Audio API — there are no audio files. A step sequencer schedules notes slightly ahead of the audio clock so timing doesn't drift with the frame rate, and the track follows the game: something sparse in the menus, driving in combat, more dissonant for bosses, and a slow fall on death.

Audio suspends whenever the page is backgrounded, the screen locks, or the tab closes. This matters on iOS, where Safari will otherwise keep a running audio context alive behind a home-screen swipe. Returning to the page resumes sound and leaves the game paused on the manual.

---

## Running it

No tooling required.

```
git clone https://github.com/ivephoton/iron-meridian.git
cd iron-meridian
open index.html
```

To publish: **Settings → Pages**, source **Deploy from a branch**, branch `main`, folder `/ (root)`. The file must be named `index.html` for Pages to serve it at the repository root.

---

## Built with

Plain JavaScript and a 480×720 canvas, scaled to fit the window. Ships, enemies and bosses are drawn as vector paths rather than sprites. Everything — game, art, music — lives in `index.html`, so the page works offline and nothing can 404.

---

## Licence

MIT.
