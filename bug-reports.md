[← Back to my profile](https://github.com/gkaragioul)

# Bug reports

Some problems can't be fixed from the outside. For those I trace the cause as far as I can, then give the developers a report they can act on: what happens and how often, the log lines that show it, and what I've already ruled out.

## Killing Floor 3 stops drawing after about a minute

[Obelisk](https://github.com/Zagrios/Obelisk) · Linux engine with D3DMetal · [Obelisk#68](https://github.com/Zagrios/Obelisk/issues/68) [![status](https://img.shields.io/github/issues/detail/state/Zagrios/Obelisk/68?label=)](https://github.com/Zagrios/Obelisk/issues/68)

Easy Anti-Cheat loads and the game opens, then the picture freezes about a minute in, in 5 of 5 launches. The log shows a Direct3D 12 queue whose work never completes, after which the device is retired as lost. The game keeps running with sound but draws nothing more.

## Easy Anti-Cheat's launcher crashes as it closes

[neptune](https://github.com/Zagrios/neptune) · Direct3D 11 · [neptune#4](https://github.com/Zagrios/neptune/issues/4) [![status](https://img.shields.io/github/issues/detail/state/Zagrios/neptune/4?label=)](https://github.com/Zagrios/neptune/issues/4)

On all three launches of Killing Floor 3, Easy Anti-Cheat's launcher crashed inside neptune's Direct3D 11 as it closed, just after reporting success. The pattern points to an object being released after its device was destroyed. I couldn't tell which object, so this is a report rather than a fix.

## Steam Cloud saves of 12 more games are rejected

[Obelisk](https://github.com/Zagrios/Obelisk) · Steam Cloud · [Obelisk#42](https://github.com/Zagrios/Obelisk/issues/42) [![status](https://img.shields.io/github/issues/detail/state/Zagrios/Obelisk/42?label=)](https://github.com/Zagrios/Obelisk/issues/42)

After fixing Quake's saves, I ran Obelisk's own rule reader over the save rules of a whole Steam library. Twelve more games, among them Papers, Please and The Last of Us Part I, are rejected, for eight different reasons. A later pull request ([#43](https://github.com/Zagrios/Obelisk/pull/43), merged) fixed five of them.

## Proposals

### Run old 32-bit games on the Linux engine, with fast x87 maths

[Obelisk](https://github.com/Zagrios/Obelisk) · [Obelisk#72](https://github.com/Zagrios/Obelisk/issues/72) [![status](https://img.shields.io/github/issues/detail/state/Zagrios/Obelisk/72?label=)](https://github.com/Zagrios/Obelisk/issues/72)

The original Killing Floor runs at 10–12 frames per second on Obelisk's Rosetta engine, because Rosetta works out the game's old x87 maths in software. The Linux engine has a mode that ran the same kind of code about 5 times faster. I proposed running 32-bit games there and did the first part myself: 32-bit programs now start on the Linux engine, merged and released in [Voile v26.3.0-25](https://github.com/Zagrios/Voile/releases/tag/v26.3.0-25).

See also: [Open-source contributions](README.md)
