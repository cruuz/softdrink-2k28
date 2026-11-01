# SOFTDRINK 2K28

SOFTDRINK 2K28 turns your own copy of ESPN NFL 2K5 (USA, Xbox) into a 2026 season disc: teams, rosters, uniforms, faces and coaches, rebuilt modern stadiums, and the 2026 ESPN presentation. It is made with the free [2K5 Mod Studio](https://github.com/cruuz/2k-football-mod-tools).

## What you need

- Your own unmodified ESPN NFL 2K5 USA disc image for the original Xbox, dumped from a disc you own, as one image file (`.iso` or `.xiso`). A raw (redump) dump or a rebuilt (repacked) image is fine; a disc someone already modded is refused. An extracted game folder is not an image file: turn it into an xiso first. Your source image stays unchanged.
- [2K5 Mod Studio beta-79](https://github.com/cruuz/2k-football-mod-tools/releases/tag/beta-79) or later for Windows, Linux or macOS.
- `SOFTDRINK-2K28-v0.8.2k5patch` from this repository's [Releases](https://github.com/cruuz/softdrink-2k28/releases), with enough free space for the new disc. The Studio checks the required space before installing.
- xemu with **System Memory set to 128 MiB** (Settings, System) and the **Complex 4627** BIOS image as the Flash ROM. Both are required for v0.8: the 4,096-player roster uses the 128 MiB memory layout, and the startup patch needs the 4627 BIOS. If you start xemu from the Studio, it warns you when either is not set.

## Install in 5 steps

1. Download **2K5 Mod Studio beta-79** and **SOFTDRINK-2K28-v0.8.2k5patch** from their release pages. Keep the patch file as downloaded; do not extract it.
2. Open Studio and go to **Build & Share → Share → Install SOFTDRINK 2K28**.
3. Select your **unmodified ESPN NFL 2K5 USA Xbox image file**, then the **`.2k5patch` file itself**. Use the original image for each update, not your v0.7 disc.
4. Choose a new output image and wait for **Disc ready**.
5. In xemu, choose **Machine → Load Disc** and select the **new image**, or click **Play latest disc in xemu** in Studio. In the game, **load the disc roster and start a fresh franchise**. Existing franchises keep their saved roster.

Set xemu System Memory to **128 MiB** with the Complex 4627 BIOS; this is required for v0.8. See the [five-step install guide](https://github.com/cruuz/2k-football-mod-tools/blob/beta-79/docs/mod_editor/install_softdrink_2k28.md) and [recommended xemu settings](https://github.com/cruuz/2k-football-mod-tools/blob/beta-79/docs/mod_editor/recommended_xemu_settings.md).

To change options or art before building, use **Customize SOFTDRINK 2K28** on the same tab. It opens the included sources and recipe in the Build tab.

From a 2k-football-mod-tools source checkout, the equivalent command is:

```sh
python tools/nfl2k5_modpack.py apply SOFTDRINK-2K28-v0.8.2k5patch --source "your disc.iso" --out "SOFTDRINK 2K28.iso"
```

## Versions

- **v0.8**: a 4,096-player roster with 450-prospect draft classes every year, undrafted players at every position, retirement by age and a smarter 53-man cut with a preseason warning; MyCareer creates a player again; real season history, years pro and real official headshots for the created free agents; CPU defenses that call their real 2025 coordinators' fronts, coverages and blitzes, coverage-only defensive audibles and modern books in Situation mode; pass rush and pass blocking by the ratings, and new stats (pressures, QB hits, sacks allowed, targets); equal catch odds for human and CPU, CPU quarterbacks who read by their ratings, and star charge-ups for every star; a Super Bowl champion and MVP notice, a champions history page that starts with every real Super Bowl from XXXIX to LX, and modern award voting; realistic simulated rushing with running back injuries, NFL pass and run balance and simulated overtime under the 2025 rule; realistic draft prospects and headshots with real bust and steal rates; the real Super Bowl, network and team-season logos, rebuilt sideline uniforms for 63 kits, a tighter Broadcast camera and kicks shown from behind the kicker, and new-profile defaults of 7-minute quarters, 15-minute sim quarters and Chop Block on. See the [v0.8 release notes](https://github.com/cruuz/softdrink-2k28/releases/tag/v0.8) for the full scope and limits.

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

v0.8 was built by the Studio from the release recipe and checked in headless emulator runs on the release disc: boot at 128 MiB and the memory screen at 64 MiB; a new MyNFL on the 4,096-record roster saved, reloaded and read back; a v0.7 franchise brought forward with Franchise > Upgrade; MyCareer Enter the Draft and Undrafted Free Agent; the preseason warning and the cut to 53; Player Cards with years pro, history, headshots and the new stats; League Leaders; the champions history page; Situation mode with the modern books and the coverage-only audible panel; the Broadcast camera on snaps, passes and kicks; sideline uniforms; Super Bowl moments; a whole simulated season to the champion and MVP notice; and a quick game. Installing the pack with the public installer reproduces the release disc byte for byte. Whole seasons were simulated in the game's own code outside the emulator for the stats quoted in the release notes.

Nobody played a full season on this disc before release. Known limits in v0.8: upgraded franchises start the champions history empty and keep the years pro, history and photos of players already in the save (start a new franchise for those; run Upgrade before the v0.8 game first saves the old franchise, or it keeps its 3,231 records), and an old franchise's first new draft can be 344 to 358 prospects; existing profiles keep their old quarter length, sim quarter and Chop Block settings; imported seasons before 2026 show 0 pressures, QB hits, sacks allowed and targets, and League Leaders shows only pressures in place of a retail column; drops are rarer than in the NFL; simulated team rushing runs a little high and 4,000-yard passers a little low; the view from behind the punter is wider when you receive the punt; the weekly Player Progress views are not reachable (the screen shows the season change); a free agent you rename or sign into a different record keeps that record's photo; a few rebuilt sideline sheets keep small flaws; the 4627 BIOS check recognises one common image by its bytes, so another working 4627 dump can show the BIOS message; 69 real players are on no club and not on the free agent list (already so in v0.7). The audible crash, invisible players in moments and a Steam Deck free agency freeze were reported and not reproduced.

Earlier limits that still apply: a club at 53 active players with a full 12-man practice squad still cannot make a 1-for-1 trade; 26 players with braids still have no hair over the top with the helmet off; the big roster header font drops the space before a suffix, so Deebo Samuel Sr. reads SAMUELSR; the Raiders down-and-distance tab is silver and the weakest of the 32; formation names are cut off in 345 of 1,108 offense play-call headers. Existing franchises keep their own ratings, colleges, announcer names, suffixes, gear and refresh-player looks, so those need a new franchise. Saves made with the 16 reserves option (724,140 bytes) do not load on the bigger-roster disc. The Crib keeps only its Trophy Room.

If installation or boot fails, keep the Studio's error message and report your Studio version, pack version, xemu version, memory setting and BIOS, and where it stops, in the project's **#2k5-bugs** Discord channel.

## What is in the pack

The patch contains mod content and installation instructions. The installer reads unchanged game data from your own disc and refuses modified or incompatible source files. The download is not a playable game image on its own. It also includes the authoring sources and recipe for customization in the Studio.

## Notes

This is an unofficial fan project, not affiliated with or endorsed by the NFL, the NFLPA, ESPN, 2K or any team. Team, league and broadcast names and marks belong to their owners.

Prepared by Claude on Noah's behalf.
