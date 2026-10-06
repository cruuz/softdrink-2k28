# SOFTDRINK 2K28

SOFTDRINK 2K28 turns your own copy of ESPN NFL 2K5 (USA, Xbox) into a 2026 season disc: teams, rosters, uniforms, faces and coaches, rebuilt modern stadiums, and the 2026 ESPN presentation. It is made with the free [2K5 Mod Studio](https://github.com/cruuz/2k-football-mod-tools).

## What you need

- Your own unmodified ESPN NFL 2K5 USA disc image for the original Xbox. Plain xiso, raw and repacked images are accepted when their game files match the supported retail files. Your source image stays unchanged.
- [2K5 Mod Studio beta 76.5](https://github.com/cruuz/2k-football-mod-tools/releases/tag/beta-76.5) or later for Windows, Linux or macOS.
- `SOFTDRINK-2K28-v0.5.2k5patch` from this repository's [Releases](https://github.com/cruuz/softdrink-2k28/releases), with enough free space for the new disc. The Studio checks the required space before installing.
- xemu. **System Memory set to 128 MB** (Settings, System) is recommended. Earlier builds could repeat the pregame show at some stadiums with the default 64 MB until you pressed A to skip it.

## Install in 5 steps

1. Download **2K5 Mod Studio beta-76.5** and **SOFTDRINK-2K28-v0.5.2k5patch** from their release pages. Keep the patch file as downloaded; do not extract it.
2. Open Studio and go to **Build & Share → Share → Install SOFTDRINK 2K28**.
3. Select your **unmodified ESPN NFL 2K5 USA Xbox image**, then the **`.2k5patch` file itself**. Use the original image for each update.
4. Choose a new output image and wait for **Disc ready**.
5. In xemu, choose **Machine → Load Disc** and select the **new image**, or click **Play latest disc in xemu** in Studio. In the game, **load the disc roster and start a fresh franchise**. Existing franchises keep their saved roster.

Set xemu System Memory to **128 MiB**. See the [five-step install guide](https://github.com/cruuz/2k-football-mod-tools/blob/beta-76.5/docs/mod_editor/install_softdrink_2k28.md) and [recommended xemu settings](https://github.com/cruuz/2k-football-mod-tools/blob/beta-76.5/docs/mod_editor/recommended_xemu_settings.md).

To change options or art before building, use **Customize SOFTDRINK 2K28** on the same tab. It opens the included sources and recipe in the Build tab.

From a 2k-football-mod-tools source checkout, the equivalent command is:

```sh
python tools/nfl2k5_modpack.py apply SOFTDRINK-2K28-v0.5.2k5patch --source "your disc.iso" --out "SOFTDRINK 2K28.iso"
```

## Versions

- **v0.5**: commentary uses available surnames or jersey numbers; the dated free-agent pool grows to 377 players, including 18 quarterbacks; the refreshed roster starts with 155 vacant records for historical imports and Create Player; modern facemasks gain cage clearance; selected uniform fonts, crowd joins, field art and end-wall play-clock digits are corrected. Anniversary has 51 chronological moments, including the Unc Bowl. The incomplete Practice Squad screen is removed. Passing and ordinary ball-carrier input changes have offline native checks and still need a gameplay check. New player ratings are estimates, appearances are generic and no new individual headshots are added. See the [v0.5 release notes](https://github.com/cruuz/softdrink-2k28/releases/tag/v0.5) for the full scope and limits.

- **v0.4**: normal and shotgun/spread personnel use the lead running back; SPECIAL PWRB has a separate order; 236 affected free agents use the native no-photo fallback instead of a repeated wrong portrait; and 135 modern stadium crowd variants have corrected spacing and billboard heights. MetLife is unchanged. The installed image matches the desktop test disc and retains its Anniversary and kickoff corrections. Load the disc roster and start a fresh franchise for the roster changes; existing saves retain their stored players and depth charts.

- **v0.3**: fixes the release of both teams on onside kicks with dynamic kickoffs enabled; corrects portraits, reviewed skin tones and star icons in the 25 added Anniversary moments; corrects the starting situations for the Tyree, Holmes and Butler moments; and includes the frozen 2 October 2026 roster update described below.
- **v0.2**: lowers the flight of deep balls while leaving throws up to 40 yards unchanged; removes the blocks of colour behind end-zone lettering at Chicago, Kansas City, Washington and Cleveland; and makes the ESPN scorebar's timeout marks dim as each team uses its timeouts.
- **v0.1**: the first release.

The roster snapshot included in v0.3 moves J.J. McCarthy from Minnesota to the Giants and places Claudin Cherelus, Odell Beckham and KhaDarel Hodge in free agency, alongside depth-chart adjustments. This describes the supplied snapshot dated 2 October, rather than a live roster feed.

Anniversary content retains the earlier portrait and star corrections. Some period field details, unavailable venues and the Unc uniforms remain documented approximations; the two new 2025 teams include 32 labeled template appearances among 106 players.

## Testing and limits

The v0.5 corrections have offline checks. Linux and Windows CPython under Wine installations reproduce the finished disc byte for byte, matching all 19 game files. One private xemu smoke reached a 2026 game, coin toss, a helmeted close-up and Broadcast view at AT&T. Commentary, motion, passing, franchise behavior and the visual changes still need a gameplay check. The disc follows verified native repairs on v0.4; a complete 116-option Studio build was not run.

The reported post-playcall hang and receiver TD graphic remain unresolved. The Vikings horn, moving Giants helmet wobble and several stadium geometry defects remain open. Original Xbox hardware is outside this release's supported scope.

If installation or boot fails, keep the Studio's error message and report your Studio version, xemu version, memory setting and where it stops in the project's **#2k5-bugs** Discord channel.

## What is in the pack

The patch contains mod content and installation instructions. The installer reads unchanged game data from your own disc and refuses modified or incompatible source files. The download is not a playable game image on its own. It also includes the authoring sources and recipe for customization in the Studio.

## Notes

This is an unofficial fan project, not affiliated with or endorsed by the NFL, the NFLPA, ESPN, 2K or any team. Team, league and broadcast names and marks belong to their owners.

Prepared for Noah (SOFTDRINKTV) with work by Claude and Codex.
