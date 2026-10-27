# Anatomy of a Successful Attack — interactive

An interactive rebuild of Ben Ruiz's essay
[Anatomy of a Successful Attack](https://aztez.com/blog/2014/01/06/anatomy-of-a-successful-attack/)
and its "Impact Effects" demo, showing how one sword hit is built from nine
layered effects fired on a precise schedule.

**Live:** https://atomechllc.github.io/anatomy-of-a-successful-attack/

## Controls

- `Z` / `Space` / click — full attack (pressing again restarts it)
- `1`–`9` — fire one ingredient by itself, as in the original demo
- checkboxes — cut layers from the full attack
- `0` — sound on/off, `R` — all layers back on

## The schedule

Taken from the demo build's scene data, in seconds after the attack starts:

| t | event |
|---|---|
| 0.00 | attack animation |
| 0.10 | swing whoosh |
| 0.20 | swing FX, foot dust, camera shake, blood |
| 0.22 | struck animation, impact sound, grunt |
| 0.23 | hit burst |
| 0.25 | impact sparks |

The hit-freeze is baked into "Hiccup" variants of the animation clips, so the
two characters hold while effects keep moving. The camera shake is smooth noise
with a sine-eased decay over 0.16 s.

## Credits and rights

The character animation, effects and sounds in `assets/aztez/` belong to
**Team Colorblind** (Aztez). They were captured from the free "Impact Effects
2015" demo that accompanies the essay, for educational use. They are not
covered by any license in this repository. If you are Team Colorblind and want
them changed or removed, open an issue.

The page code (`index.html`, `attack.css`, `attack.js`) is by Atomech.
