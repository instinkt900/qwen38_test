# Scorched Earth

A single-file recreation of the classic artillery game. No dependencies, no build step.

## Run

Open `index.html` in any modern browser. That's it.

If your browser blocks it as a local file, serve the directory instead:

    python3 -m http.server 8000

then visit http://localhost:8000.

## How to play

Pick a mode from the menu:

- **Solo** — you vs 3 AI tanks (rookie / normal / expert).
- **Pass & play** — 2 to 4 tanks, one keyboard. Between turns an overlay tells the next player to pass the keyboard; press Enter to take over.

### Controls (your turn)

| Key | Action |
|---|---|
| Left / Right arrows (or A/D) | move tank |
| Up / Down arrows (or W/S) | aim |
| + / − (or = / -) | shell power |
| 1–7 | select shell type |
| Space or Enter | fire |
| P or Esc | pause |
| M | mute |

### Shells

| # | Shell | Effect |
|---|---|---|
| 1 | Shell | standard explosion (34 damage) |
| 2 | Big gun | large blast (62 damage), knockback |
| 3 | Smart | homes on the nearest enemy after ~0.35 s of flight |
| 4 | Napalm | leaves fire that burns terrain and tanks |
| 5 | Parachute | drops an extra tank (max 8 alive) |
| 6 | Satellite | reveals enemy tank positions for a few turns |
| 7 | Mine | buries a persistent mine that also burns terrain |

You start with 4 smart shells; other types come in a random stock of 0–3 each. Destroy the other tanks to win.

### Notes

- Wind changes every turn and bends shells while they fly — it's shown in the top bar.
- The day/night cycle is cosmetic.
- Terrain is fully destructible, and fire and mines erode it over time.

## Files

- `index.html` — the entire game (markup, style, logic, audio synth).
