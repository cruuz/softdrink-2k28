# SOFTDRINK 2K28

SOFTDRINK 2K28 turns your own copy of ESPN NFL 2K5 (USA, Xbox) into a 2026 season disc: teams, rosters, uniforms, faces and coaches, rebuilt modern stadiums, and the 2026 ESPN presentation. It is made with the free [2K5 Mod Studio](https://github.com/cruuz/2k-football-mod-tools).

## What you need

- Your own unmodified ESPN NFL 2K5 USA disc image for the original Xbox, dumped from a disc you own. Use an untouched `.iso` or `.xiso`; a modified disc or a rebuilt image is refused. Your source image stays unchanged.
- [2K5 Mod Studio beta-78](https://github.com/cruuz/2k-football-mod-tools/releases/tag/beta-78) or later for Windows, Linux or macOS.
- `SOFTDRINK-2K28-v0.7.2k5patch` from this repository's [Releases](https://github.com/cruuz/softdrink-2k28/releases), with enough free space for the new disc. The Studio checks the required space before installing.
- xemu. **System Memory set to 128 MiB** (Settings, System) is required for v0.7: the bigger roster uses the 128 MiB memory layout. At 64 MiB a Quick Game at the retail-model Acrisure stadium loops the pregame. Use 128 MiB.

## Install in 5 steps

1. Download **2K5 Mod Studio beta-78** and **SOFTDRINK-2K28-v0.7.2k5patch** from their release pages. Keep the patch file as downloaded; do not extract it.
2. Open Studio and go to **Build & Share → Share → Install SOFTDRINK 2K28**.
3. Select your **unmodified ESPN NFL 2K5 USA Xbox image**, then the **`.2k5patch` file itself**. Use the original image for each update.
4. Choose a new output image and wait for **Disc ready**.
5. In xemu, choose **Machine → Load Disc** and select the **new image**, or click **Play latest disc in xemu** in Studio. In the game, **load the disc roster and start a fresh franchise**. Existing franchises keep their saved roster.

Set xemu System Memory to **128 MiB**; this is required for v0.7. See the [five-step install guide](https://github.com/cruuz/2k-football-mod-tools/blob/beta-78/docs/mod_editor/install_softdrink_2k28.md) and [recommended xemu settings](https://github.com/cruuz/2k-football-mod-tools/blob/beta-78/docs/mod_editor/recommended_xemu_settings.md).

To change options or art before building, use **Customize SOFTDRINK 2K28** on the same tab. It opens the included sources and recipe in the Build tab.

From a 2k-football-mod-tools source checkout, the equivalent command is:

```sh
python tools/nfl2k5_modpack.py apply SOFTDRINK-2K28-v0.7.2k5patch --source "your disc.iso" --out "SOFTDRINK 2K28.iso"
```

## Versions

- **v0.7**: 533 real unsigned NFL players join free agency on a bigger roster, with CPU clubs restructuring contracts, keeping their stars and staying at 50 players; NFL-like aging and retirement by position, weekly progression, rookie stars, stars earned and lost over a career, and a working Player Progress screen; 3,569 new rookie faces that follow each prospect, rarer names and suffixes, a broadcast-paced draft and a very rare gray alien prospect; CPU clock management that kneels, calls timeouts and goes for it late, better third-down and short-yardage calls, and runners who stay in bounds; pass protection, kick coverage, the modern force-out rule, simulated games at NFL pace, higher Throw Power and a mid-game Choose Side that no longer crashes; scorebug, SportsCenter, stadium board, play clock, turf and crowd cutaway fixes, team-coloured sleeves, dreads and locs with hair over the top, real suffixes, corrected colleges and announcer names, and scanned faces for all 32 head coaches; the Crib cut down to a Trophy Room, and the 2006 Sarasota Seamen as a classic team. It fixes the reported Contracts and Free Agents freeze, MyCareer with a custom name, the Studio Build tab, trades through Week 9 and the two-minute warning. See the [v0.7 release notes](https://github.com/cruuz/softdrink-2k28/releases/tag/v0.7) for the full scope and limits.

- **v0.6.1**: fixes the defensive play-call menu freeze, the MyCareer Fast Forward crash and the MyCareer depth chart freeze, and adds rebuilt playbooks with about 1.76 times the original game's plays per team book, accurate short throws and longer run blocking, 149 classic teams, new 25th Anniversary moments with 105 more face scans, the 2026 head coaches and officials, 2026 fans, and a rebuilt U.S. Bank Stadium exterior. See the [v0.6.1 release notes](https://github.com/cruuz/softdrink-2k28/releases/tag/v0.6.1).

- **v0.6**: adds rebuilt 32-team modern offense and defense books with team packages, Modern 2 CPU decisions, stars-only player abilities, letter grades and a franchise honors page, corrected experience and higher Throw Power, plus Anniversary menu, uniform and venue corrections, primary, alternate and throwback uniform work, modern goalposts, retuned rain and an Allegiant Stadium rebuild. Its editable source recipe was not certified to rebuild the disc. See the [v0.6 release notes](https://github.com/cruuz/softdrink-2k28/releases/tag/v0.6).

- **v0.5**: commentary uses available surnames or jersey numbers; the dated free-agent pool grows to 377 players, including 18 quarterbacks; the refreshed roster starts with 155 vacant records for historical imports and Create Player; modern facemasks gain cage clearance; selected uniform fonts, crowd joins, field art and end-wall play-clock digits are corrected. Anniversary has 51 chronological moments, including the Unc Bowl. The incomplete Practice Squad screen is removed. Passing and ordinary ball-carrier input changes have offline native checks and still need a gameplay check. New player ratings are estimates, appearances are generic and no new individual headshots are added. See the [v0.5 release notes](https://github.com/cruuz/softdrink-2k28/releases/tag/v0.5) for the full scope and limits.

- **v0.4**: normal and shotgun/spread personnel use the lead running back; SPECIAL PWRB has a separate order; 236 affected free agents use the native no-photo fallback instead of a repeated wrong portrait; and 135 modern stadium crowd variants have corrected spacing and billboard heights. MetLife is unchanged. The installed image matches the desktop test disc and retains its Anniversary and kickoff corrections. Load the disc roster and start a fresh franchise for the roster changes; existing saves retain their stored players and depth charts.

- **v0.3**: fixes the release of both teams on onside kicks with dynamic kickoffs enabled; corrects portraits, reviewed skin tones and star icons in the 25 added Anniversary moments; corrects the starting situations for the Tyree, Holmes and Butler moments; and includes the frozen 2 October 2026 roster update described below.
- **v0.2**: lowers the flight of deep balls while leaving throws up to 40 yards unchanged; removes the blocks of colour behind end-zone lettering at Chicago, Kansas City, Washington and Cleveland; and makes the ESPN scorebar's timeout marks dim as each team uses its timeouts.
- **v0.1**: the first release.

The roster snapshot included in v0.3 moves J.J. McCarthy from Minnesota to the Giants and places Claudin Cherelus, Odell Beckham and KhaDarel Hodge in free agency, alongside depth-chart adjustments. This describes the supplied snapshot dated 2 October, rather than a live roster feed.

Anniversary content retains the earlier portrait and star corrections. Some period field details, unavailable venues and the Unc uniforms remain documented approximations; the two new 2025 teams include 32 labeled template appearances among 106 players.

## Testing and limits

v0.7 was checked by 49 scripted headless emulator runs, 36 on the first release candidate and 13 on the final disc. Every boot reached the main menu in about 57 seconds, and the 14 minute attract demo ran without a freeze. Choose Side worked once and three times in a row. Full and partial games ran without a freeze: Eagles at Ravens (both halves), Seahawks at Jaguars, Bills at Patriots in snow, Buccaneers at Colts, Packers at Vikings at U.S. Bank Stadium, the Seamen, and forced two-minute and fourth-down situations. On the final disc a new franchise opened Player Progress, built a trade, signed a free agent, saved and reloaded three times and simulated to Week 10, with trades and the trading block closed after the Week 9 deadline; a preseason trade reached the confirm dialog and got a CPU reply. A MyCareer save loaded and played into its Week 4 game. Stadium loads reached play at M&T Bank (day and night), MetLife (flurries), Paycor, Empower Field and Lincoln Financial Field. The regression found one freeze on the first candidate, opening Player Progress in a brand-new franchise, which is fixed on the final disc. The earlier round-one test disc also passed its automated regression, including 24 Quick Game loads, MyCareer loads and a custom-name draft, a franchise through 12 simulated weeks with all 32 depth charts checked, Situation at MetLife and the Contracts lists.

Nobody played a full season on this disc before release. The automated runs did not cover 64 MiB stadium loads, the Unc Bowl, every Anniversary moment, or a full season. Not witnessed in a game: a save written and reloaded after an accepted in-season trade (the Week 8 acceptance was seen in memory), a new MyCareer save on the bigger roster, the late fourth-down rule in a natural game, the third-down change after the fix, the CPU sprint bursts, the SportsCenter lineup fix rendered on screen, and five Choose Side switches in a row. Return coverage and pass protection were measured on small samples only, so if returns or sacks feel wrong, report the game mode, teams and quarter length.

Known limits: a club at 53 active players with a full 12-man practice squad still cannot make a 1-for-1 trade; a simulated playoff game still uses sudden death overtime and can end on the first score; 26 players with braids still have no hair over the top with the helmet off; the big roster header font drops the space before a suffix, so Deebo Samuel Sr. reads SAMUELSR; the Raiders down-and-distance tab is silver and the weakest of the 32; formation names are cut off in 345 of 1,108 offense play-call headers; Tush Push lag was not measured. All 32 head coaches have scanned faces, with a few colour and edge limits described in the release notes. Existing franchises keep their own ratings, colleges, announcer names, suffixes, gear and refresh-player looks, so those need a new franchise; Franchise > Upgrade covers years pro, playbooks, team history, coaches, hair styles, honors and free agents. Saves made with the 16 reserves option (724,140 bytes) do not load on the bigger-roster disc. At 64 MiB a Quick Game at the retail-model Acrisure stadium loops the pregame, so use 128 MiB. The Crib keeps only its Trophy Room, and Player Progress records your club's games only; its new-season reset is unit-tested, not played. Not built this time: the Lions helmet decal shown twice in SportsCenter, the Cap Manager highest-paid order, Owner's Mode and a user Restructure button.

The scorebug ticker report came from a PC recompiled build, which this project does not support. A Vikings home game freezing during delay-of-game penalties and a receiver running his route to the bench once on an unset depth chart were not reproduced. If installation or boot fails, keep the Studio's error message and report your Studio version, pack version, xemu version, memory setting and where it stops in the project's **#2k5-bugs** Discord channel.

## What is in the pack

The patch contains mod content and installation instructions. The installer reads unchanged game data from your own disc and refuses modified or incompatible source files. The download is not a playable game image on its own. It also includes the authoring sources and recipe for customization in the Studio.

## Notes

This is an unofficial fan project, not affiliated with or endorsed by the NFL, the NFLPA, ESPN, 2K or any team. Team, league and broadcast names and marks belong to their owners.

Prepared by Claude on Noah's behalf.
