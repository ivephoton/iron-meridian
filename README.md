# Iron Meridian

A vertical scrolling shooter in the Raiden mould. One HTML file, no build step, no dependencies — open `index.html` in a browser and fly.

**[Play it here](https://ivephoton.github.io/iron-meridian/)**

## Controls

| | |
|---|---|
| Move | Arrow keys or WASD, or drag anywhere on screen |
| Fire | Z, J or space — hold it. Touch fires automatically |
| Bomb | X or K, or the pad in the bottom right on touch |
| Precision | Hold shift or C to halve your speed and reveal your hitbox |
| Pause / mute | P / M. On touch, the pip in the top right pauses |

Only the glowing core takes hits, not the whole ship. Hold precision to see exactly where it is.

## Weapons

Five of them, each with five power levels.

- **Vulcan** — spread cannon, widening from one shot to five
- **Lance** — piercing beams that drill through a whole column
- **Plasma** — slow orbs that detonate with splash damage
- **Hornet** — seeking warheads plus a light nose gun
- **Arc** — chain lightning that picks its own targets and jumps between them

A lettered pod swaps your weapon; picking up your current letter, or a gold P, raises its level. Switching costs you a level, so a pod you don't want is worth dodging. At level five the pods pay out points instead. A blue B is a spare bomb, and a green 1 is a spare ship.

Bombs clear every bullet on screen for points, hit everything alive for heavy damage, and leave you briefly untouchable. Dying costs you a life and a weapon level.

## Pilots

Five, with real trade-offs rather than palette swaps.

| Pilot | Character |
|---|---|
| Falcon | Balanced. No weaknesses, no gimmicks |
| Bolt | Fastest ship, smallest hitbox, one fewer life |
| Aegis | Spare ship and spare bomb, sluggish turns |
| Havoc | 65% more damage at half the fire rate |
| Nyx | Enormous fire rate, feather-light shots, two extra bombs |

## Difficulty

Cadet, Regular and Meridian change bullet speed, enemy fire intervals, hull HP, formation density, drop rate, boss HP, and how many ships you start with (5 / 3 / 2).

## Structure

Waves escalate endlessly and pay a bonus when cleared. Every fifth wave is a boss, drawn from four designs — Anvil, Sentinel, Hydra and Warden — each with three attack phases that switch at two thirds and one third of its health. Come back round to a design you've already beaten and it returns considerably tougher.

Killing enemies in quick succession builds a chain multiplier, up to eight times score. Stop shooting for more than a second and it lapses. Dying resets it outright.

The best score lasts as long as the tab does; nothing is written to disk.

## Running it

No tooling required. Clone and open the file:

```
git clone https://github.com/ivephoton/iron-meridian.git
cd iron-meridian
open index.html
```

To publish it: in the repository, go to Settings → Pages, and set the source to the `main` branch, root folder.

## Built with

Plain JavaScript and a 480×720 canvas. Ships, enemies and bosses are drawn as vector paths; sound is synthesised with the Web Audio API. Everything lives in `index.html`.

## Licence

MIT.
