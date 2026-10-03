# SOFTDRINK 2K28

SOFTDRINK 2K28 turns your own copy of ESPN NFL 2K5 (USA, Xbox) into a 2026 season disc: teams, rosters, uniforms, faces and coaches, rebuilt modern stadiums, and the 2026 ESPN presentation. It is made with the free [2K5 Mod Studio](https://github.com/cruuz/2k-football-mod-tools).

## What you need

- Your own unmodified ESPN NFL 2K5 USA disc image for the original Xbox. Plain xiso, raw and repacked images are accepted when their game files match the supported retail files. Your source image stays unchanged.
- [2K5 Mod Studio beta 76.3](https://github.com/cruuz/2k-football-mod-tools/releases/tag/beta-76.3) or later for Windows, Linux or macOS.
- `SOFTDRINK-2K28-v0.3.2k5patch` from this repository's [Releases](https://github.com/cruuz/softdrink-2k28/releases), with enough free space for the new disc. The Studio checks the required space before installing.
- xemu. **System Memory set to 128 MB** (Settings, System) is recommended. Earlier builds could repeat the pregame show at some stadiums with the default 64 MB until you pressed A to skip it.

## Install

1. Open 2K5 Mod Studio and go to the Share tab.
2. Click **Install SOFTDRINK 2K28**, select your unmodified ESPN NFL 2K5 disc image and the v0.3 patch, and choose a new output image.
3. Wait for installation and verification to finish. The Studio checks every game file before keeping the new image.

Open the new image in xemu. Install each pack version directly from retail; do not apply v0.3 over a v0.1 or v0.2 image.

To change options or art before building, use **Customize SOFTDRINK 2K28** on the same tab. It opens the included sources and recipe in the Build tab.

From a 2k-football-mod-tools source checkout, the equivalent command is:

```sh
python tools/nfl2k5_modpack.py apply SOFTDRINK-2K28-v0.3.2k5patch --source "your disc.iso" --out "SOFTDRINK 2K28.iso"
```

## Versions

- **v0.3**: fixes the release of both teams on onside kicks with dynamic kickoffs enabled; corrects portraits, reviewed skin tones and star icons in the 25 added Anniversary moments; corrects the starting situations for the Tyree, Holmes and Butler moments; and includes the frozen 2 October 2026 roster update described below.
- **v0.2**: lowers the flight of deep balls while leaving throws up to 40 yards unchanged; removes the blocks of colour behind end-zone lettering at Chicago, Kansas City, Washington and Cleveland; and makes the ESPN scorebar's timeout marks dim as each team uses its timeouts.
- **v0.1**: the first release.

The roster snapshot included in v0.3 moves J.J. McCarthy from Minnesota to the Giants and places Claudin Cherelus, Odell Beckham and KhaDarel Hodge in free agency, alongside depth-chart adjustments. This describes the supplied snapshot dated 2 October, rather than a live roster feed.

The 25 added Anniversary moments now use a player's own available portrait or no portrait, and preserve star icons for players rated 90 or better. Twenty of the 2,544 players have no reviewed skin-tone source and keep their previous tone. The 25 original retail moments do not receive this new portrait correction. Era-specific uniforms, Super Bowl field logos and era walls remain unfinished.

## Testing and limits

The v0.3 gameplay corrections have been checked offline. This build has not yet been played in game; the earlier v0.2 lab results do not establish v0.3 gameplay behavior. See the [v0.3 release notes](https://github.com/cruuz/softdrink-2k28/releases/tag/v0.3) for its installation checks and any later observations. Original Xbox hardware is outside this release's supported scope.

If installation or boot fails, keep the Studio's error message and report your Studio version, xemu version, memory setting and where it stops in the project's **#2k5-bugs** Discord channel.

## What is in the pack

The patch contains mod content and installation instructions. The installer reads unchanged game data from your own disc and refuses modified or incompatible source files. The download is not a playable game image on its own. It also includes the authoring sources and recipe for customization in the Studio.

## Notes

This is an unofficial fan project, not affiliated with or endorsed by the NFL, the NFLPA, ESPN, 2K or any team. Team, league and broadcast names and marks belong to their owners.

Prepared for Noah (SOFTDRINKTV) with work by Claude and Codex.
