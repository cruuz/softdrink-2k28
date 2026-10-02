# SOFTDRINK 2K28

SOFTDRINK 2K28 turns your own copy of ESPN NFL 2K5 (USA, Xbox) into a 2026 season disc: the 2026 teams, rosters,
uniforms, faces and coaches, rebuilt modern stadiums, the 2026 ESPN presentation and the rest of the SOFTDRINK
changes. It is made with the free 2K5 Mod Studio from
[2k-football-mod-tools](https://github.com/cruuz/2k-football-mod-tools).

## What you need

- Your own disc image of ESPN NFL 2K5 (USA) for the original Xbox. Any common dump works: a plain xiso, a raw dump,
  or a repacked image. It is never changed.
- 2K5 Mod Studio from [beta-76.2](https://github.com/cruuz/2k-football-mod-tools/releases/tag/beta-76.2) or later
  (Windows, Linux or macOS). Beta 76 and 76.1 can install it too.
- The `.2k5patch` file from this repository's [Releases](../../releases), and about 6 GB of free space for the new disc.
- xemu with **System Memory set to 128 MB** (Settings, System) is recommended: the disc uses the extra memory for room in the pregame. It also runs at the default 64 MB, but at some stadiums the pregame show then repeats until you press A to skip it.

## Install

1. Open 2K5 Mod Studio and go to the Share tab.
2. Click **Install SOFTDRINK 2K28**, pick your ESPN NFL 2K5 disc image and the `.2k5patch` file, and choose where to
   save the new disc.
3. Wait about a minute. Every file is checked against the finished disc before the new image is kept.

Play the new image in xemu. It has not been tested on a real Xbox yet. To change something first (leave the new
stadiums out, swap art, change any option), use **Customize SOFTDRINK 2K28** on the same tab: it opens everything the
disc was built from in the Build tab.

If the new image does not boot: use xemu 0.8.136 or later (the version it was tested on), set System Memory to
128 MB, and check the image is complete (its size matches the one the Studio reports, and the Studio verified
every file before keeping it). Then post your xemu version, memory setting and where it stops in the Discord.

Command line instead of the Studio: `python tools/nfl2k5_modpack.py apply SOFTDRINK-2K28-v0.2.2k5patch --source "your disc.iso"
--out "SOFTDRINK 2K28.iso"` from the 2k-football-mod-tools folder.

## Versions

- **v0.2**: deep balls no longer fly as high as a punt (throws up to 40 yards are unchanged); the end zones at
  Chicago, Kansas City, Washington and Cleveland no longer have a block of colour behind the lettering; the ESPN
  scorebar's timeout marks dim as each team uses its timeouts. Everything else is the same as v0.1.
- **v0.1**: the first release.

Always install the newest version from your own retail image.

## What is in the pack

Only the new content and instructions. Every byte of the original game is read from your own disc while installing;
the pack stores no original game data (checked by scanning every stored 4 KiB block against the retail files). Its
manifest pins the exact retail files it expects, so a modified or wrong disc is refused with an explanation.

## Notes

This is an unofficial fan project, not affiliated with or endorsed by the NFL, the NFLPA, ESPN, 2K or any team. Team,
league and broadcast names and marks belong to their owners.

Prepared and published by Claude (Anthropic's AI assistant) for Noah (SOFTDRINKTV). Bug reports: the #2k5-bugs
channel on the project's Discord.
