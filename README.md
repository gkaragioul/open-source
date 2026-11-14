[← Back to my profile](https://github.com/gkaragioul)

# Open-source contributions

I play games on a Mac. When one doesn't work, I trace the problem to its cause, fix it, and send the fix to the project's developers with the evidence they need to check it quickly.

<table>
<tr>
<td align="center" width="25%"><h1>16</h1>merged</td>
<td align="center" width="25%"><h1>15</h1>in review</td>
<td align="center" width="25%"><h1>8</h1>projects</td>
<td align="center" width="25%"><h1>2</h1>releases credit me</td>
</tr>
</table>

<sub>Counted on 14 November 2026. The status badges below update live from GitHub.</sub>

## Soldier of Fortune on the Mac · [openMERC](https://github.com/sidreshot/openMERC)

<img src="https://raw.githubusercontent.com/gkaragioul/mac-ports/main/images/soldier-of-fortune-ambush.jpg" alt="Soldier of Fortune running natively on a Mac: three enemies come through a door in the New York subway" width="100%">

openMERC is an open-source engine for Raven Software's Soldier of Fortune (2000). I made it build and run natively on Apple silicon Macs. Then I wrote a check that walks the player up to every enemy in every level, about 1,560 of them, and lists the ones that never react. Its findings became fixes: enemies riding a train who never fought, an enemy stuck under a low ceiling, and a crash when the next level loads.

**Result:** 7 pull requests merged in two days, 12–13 November 2026. The developer repeated the fixes on Linux before merging them.

> "A really nice find, and the write-up made it quick to check." <br><sub>openMERC's developer, on [#22](https://github.com/sidreshot/openMERC/pull/22)</sub>

<details>
<summary><b>All 8 pull requests</b> · 7 merged, 1 in review</summary>
<br>

openMERC's developer merges by hand, so GitHub lists these as closed; the "merged" badges link to the commit in openMERC.

| Contribution | Pull request | Status |
|---|---|---|
| A crouching enemy that never took a step now stands up to move | [#23](https://github.com/sidreshot/openMERC/pull/23) | [![status](https://img.shields.io/github/pulls/detail/state/sidreshot/openMERC/23?label=)](https://github.com/sidreshot/openMERC/pull/23) |
| An enemy under a low ceiling now moves instead of standing still | [#22](https://github.com/sidreshot/openMERC/pull/22) | [![merged](https://img.shields.io/badge/merged-blueviolet)](https://github.com/sidreshot/openMERC/commit/72126bed47f8c586134a63037785cb6fa08e8b0f) |
| The enemies riding the train now fight back | [#21](https://github.com/sidreshot/openMERC/pull/21) | [![merged](https://img.shields.io/badge/merged-blueviolet)](https://github.com/sidreshot/openMERC/commit/7a194b13125a4240608e7eceeed7997b4a2ed89a) |
| Loading the next level no longer crashes the game | [#19](https://github.com/sidreshot/openMERC/pull/19) | [![merged](https://img.shields.io/badge/merged-blueviolet)](https://github.com/sidreshot/openMERC/commit/212d2a6245e8d78541e8ad1aab6e7c0a7ad2918e) |
| The game finds its files when started with `-basedir` or `-cddir` | [#18](https://github.com/sidreshot/openMERC/pull/18) | [![merged](https://img.shields.io/badge/merged-blueviolet)](https://github.com/sidreshot/openMERC/commit/d874b49418d6ff1dbd71529c7be58f60236c35b3) |
| The enemy check carries on when a level ends itself, hangs or crashes | [#17](https://github.com/sidreshot/openMERC/pull/17) | [![merged](https://img.shields.io/badge/merged-blueviolet)](https://github.com/sidreshot/openMERC/commit/1bd917380b145a1d47a8c04c30cfffaa7996241e) |
| A check that every enemy in a level reacts to the player | [#16](https://github.com/sidreshot/openMERC/pull/16) | [![merged](https://img.shields.io/badge/merged-blueviolet)](https://github.com/sidreshot/openMERC/commit/3daac37201e374721eb84086e7d45d6b3c18a7d7) |
| Soldier of Fortune's engine builds and runs natively on Apple silicon Macs | [#14](https://github.com/sidreshot/openMERC/pull/14) | [![merged](https://img.shields.io/badge/merged-blueviolet)](https://github.com/sidreshot/openMERC/commit/fd10caa5df69f4645806154f8b61858bd211583c) |

</details>

## Windows games on the Mac · [Obelisk](https://github.com/Zagrios/Obelisk) and its engine

Obelisk is a Mac launcher that runs Windows games from Steam, Epic and GOG. Its runtime, [Voile](https://github.com/Zagrios/Voile), has a Linux engine ([voile-lkd](https://github.com/Zagrios/voile-lkd), [voile-wine](https://github.com/Zagrios/voile-wine) and [neptune](https://github.com/Zagrios/neptune)) for games whose anti-cheat supports Linux.

- **Steam Cloud saves.** Quake's saves didn't sync. I traced it to how Obelisk reads a game's save rules, fixed it, then checked a whole Steam library and fixed five more games.
- **32-bit games on the Linux engine.** Three pull requests across Voile, voile-wine and voile-lkd let 32-bit Windows programs start, open their windows and play sound there.
- **Game videos.** Games on the Linux engine play their videos and in-game movies through GStreamer.
- **Smaller fixes.** A Plague Tale: Innocence renders, Force Quit also ends the game, and Obelisk installs with `brew install --cask obelisk`.
- **In review.** Smoother frames with an optional frame lock, OpenGL for 32-bit games, fixes for Killing Floor and Killing Floor 3, and a test for Hunt: Showdown 1896.

**Credited by name in two release notes:** [Obelisk 0.6.0](https://github.com/Zagrios/Obelisk/releases/tag/v0.6.0) (Steam Cloud saves) and [Voile v26.3.0-25](https://github.com/Zagrios/Voile/releases/tag/v26.3.0-25) (32-bit programs and game videos).

<details>
<summary><b>All 22 pull requests</b> · 9 merged, 13 in review</summary>
<br>

| Project | Contribution | Pull request | Status |
|---|---|---|---|
| [Obelisk](https://github.com/Zagrios/Obelisk) | Killing Floor's frame lock turns on by itself (draft, it depends on the PRs below) | [#80](https://github.com/Zagrios/Obelisk/pull/80) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Obelisk/80?label=)](https://github.com/Zagrios/Obelisk/pull/80) |
| [voile-lkd](https://github.com/Zagrios/voile-lkd) | A game can ask for a steady frame rate that suits the player's screen | [#23](https://github.com/Zagrios/voile-lkd/pull/23) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-lkd/23?label=)](https://github.com/Zagrios/voile-lkd/pull/23) |
| [voile-wine](https://github.com/Zagrios/voile-wine) | OpenGL frames cost less to show, with an optional frame lock | [#15](https://github.com/Zagrios/voile-wine/pull/15) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-wine/15?label=)](https://github.com/Zagrios/voile-wine/pull/15) |
| [neptune](https://github.com/Zagrios/neptune) | OpenGL frames are copied without making the game wait | [#11](https://github.com/Zagrios/neptune/pull/11) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/neptune/11?label=)](https://github.com/Zagrios/neptune/pull/11) |
| [Obelisk](https://github.com/Zagrios/Obelisk) | 32-bit games on the Linux engine draw on the Mac's GPU through OpenGL | [#79](https://github.com/Zagrios/Obelisk/pull/79) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Obelisk/79?label=)](https://github.com/Zagrios/Obelisk/pull/79) |
| [Voile](https://github.com/Zagrios/Voile) | The Linux engine's Wine is built with OpenGL | [#4](https://github.com/Zagrios/Voile/pull/4) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Voile/4?label=)](https://github.com/Zagrios/Voile/pull/4) |
| [neptune](https://github.com/Zagrios/neptune) | The render server can run OpenGL on the Mac's GPU | [#10](https://github.com/Zagrios/neptune/pull/10) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/neptune/10?label=)](https://github.com/Zagrios/neptune/pull/10) |
| [voile-wine](https://github.com/Zagrios/voile-wine) | OpenGL games' frames reach the window on the Linux engine | [#14](https://github.com/Zagrios/voile-wine/pull/14) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-wine/14?label=)](https://github.com/Zagrios/voile-wine/pull/14) |
| [voile-lkd](https://github.com/Zagrios/voile-lkd) | A test that shows the CPU information Hunt: Showdown 1896 reads is missing from the Linux engine | [#22](https://github.com/Zagrios/voile-lkd/pull/22) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-lkd/22?label=)](https://github.com/Zagrios/voile-lkd/pull/22) |
| [voile-lkd](https://github.com/Zagrios/voile-lkd) | Fixes view jumps, the pointer being pulled back after Cmd-Tab, and a fullscreen start-up crash | [#21](https://github.com/Zagrios/voile-lkd/pull/21) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-lkd/21?label=)](https://github.com/Zagrios/voile-lkd/pull/21) |
| [voile-lkd](https://github.com/Zagrios/voile-lkd) | The mouse lands in the right place when picture and window sizes differ | [#20](https://github.com/Zagrios/voile-lkd/pull/20) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-lkd/20?label=)](https://github.com/Zagrios/voile-lkd/pull/20) |
| [voile-lkd](https://github.com/Zagrios/voile-lkd) | Force Quit also ends the game | [#19](https://github.com/Zagrios/voile-lkd/pull/19) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-lkd/19?label=)](https://github.com/Zagrios/voile-lkd/pull/19) |
| [voile-lkd](https://github.com/Zagrios/voile-lkd) | Steam server lists no longer freeze the game | [#18](https://github.com/Zagrios/voile-lkd/pull/18) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-lkd/18?label=)](https://github.com/Zagrios/voile-lkd/pull/18) |
| [Voile](https://github.com/Zagrios/Voile) | Builds the 32-bit Windows parts that 32-bit games need on the Linux engine | [#3](https://github.com/Zagrios/Voile/pull/3) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Voile/3?label=)](https://github.com/Zagrios/Voile/pull/3) |
| [voile-wine](https://github.com/Zagrios/voile-wine) | 32-bit programs get display and sound on the Linux engine | [#4](https://github.com/Zagrios/voile-wine/pull/4) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-wine/4?label=)](https://github.com/Zagrios/voile-wine/pull/4) |
| [voile-lkd](https://github.com/Zagrios/voile-lkd) | 32-bit programs can start on the Linux engine (merged with the developer's changes) | [#5](https://github.com/Zagrios/voile-lkd/pull/5) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/voile-lkd/5?label=)](https://github.com/Zagrios/voile-lkd/pull/5) |
| [Obelisk](https://github.com/Zagrios/Obelisk) | A Plague Tale: Innocence renders through DXMT | [#70](https://github.com/Zagrios/Obelisk/pull/70) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Obelisk/70?label=)](https://github.com/Zagrios/Obelisk/pull/70) |
| [Homebrew](https://github.com/Homebrew/homebrew-cask) | Obelisk becomes installable with `brew install --cask obelisk` | [#299745](https://github.com/Homebrew/homebrew-cask/pull/299745) | [![status](https://img.shields.io/github/pulls/detail/state/Homebrew/homebrew-cask/299745?label=)](https://github.com/Homebrew/homebrew-cask/pull/299745) |
| [Voile](https://github.com/Zagrios/Voile) | Windows games can play their videos, through GStreamer | [#2](https://github.com/Zagrios/Voile/pull/2) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Voile/2?label=)](https://github.com/Zagrios/Voile/pull/2) |
| [Obelisk](https://github.com/Zagrios/Obelisk) | Direct3D 12 games that ship the Agility SDK, such as Killing Floor 3, render on the Linux engine | [#67](https://github.com/Zagrios/Obelisk/pull/67) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Obelisk/67?label=)](https://github.com/Zagrios/Obelisk/pull/67) |
| [Obelisk](https://github.com/Zagrios/Obelisk) | Steam Cloud saves now sync for five games whose rules use different capitalisation | [#43](https://github.com/Zagrios/Obelisk/pull/43) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Obelisk/43?label=)](https://github.com/Zagrios/Obelisk/pull/43) |
| [Obelisk](https://github.com/Zagrios/Obelisk) | Steam Cloud saves now sync for games whose rules list the "all" platform, such as Quake | [#36](https://github.com/Zagrios/Obelisk/pull/36) | [![status](https://img.shields.io/github/pulls/detail/state/Zagrios/Obelisk/36?label=)](https://github.com/Zagrios/Obelisk/pull/36) |

</details>

## Time Crisis on the Mac · [namco22-decompile](https://github.com/spacestate1/namco22-decompile)

namco22-decompile translates the arcade code of Namco's System 22 and System 23 games into C. I added native Mac builds of Time Crisis and Time Crisis II, drawn with Metal, with the tests that check the Metal drawing.

| Contribution | Pull request | Status |
|---|---|---|
| Native Mac port of Time Crisis and Time Crisis II, drawn with Metal | [#99](https://github.com/spacestate1/namco22-decompile/pull/99) | [![status](https://img.shields.io/github/pulls/detail/state/spacestate1/namco22-decompile/99?label=)](https://github.com/spacestate1/namco22-decompile/pull/99) |

## How I send a contribution

- **Small and separate.** One problem per pull request, so each can be checked and merged on its own.
- **Shown before it's fixed.** Where I can, I show the problem on the project's own unchanged code first, then the same check passing with the fix.
- **Plain language.** I explain the problem in words anyone can follow before the technical detail.

See also: [Bug reports](bug-reports.md), for problems I traced and reported.
