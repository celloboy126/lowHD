# lowHD

Diablo II: Resurrected performance mods by **celloboy126** on jsp, Nexus Mods and Traderie.

lowHD reduces visual content to help lower memory use and improve performance, especially when running multiple accounts. This repository distributes the author’s main, filler, min and partial variants, with shader binaries where supplied.

## Downloads

Download the ZIP assets from [Releases](https://github.com/celloboy126/lowHD/releases/latest), rather than GitHub’s automatic source-code archive:

- [lowHDmain.zip](https://github.com/celloboy126/lowHD/releases/latest/download/lowHDmain.zip)
- [lowHDfiller.zip](https://github.com/celloboy126/lowHD/releases/latest/download/lowHDfiller.zip)
- [lowHDmin.zip](https://github.com/celloboy126/lowHD/releases/latest/download/lowHDmin.zip)
- [lowHDpartial.zip](https://github.com/celloboy126/lowHD/releases/latest/download/lowHDpartial.zip)

## Installation

1. Extract your chosen package into the D2R `mods` folder. For example: `mods/lowHDmain/lowHDmain.mpq/modinfo.json`.
2. Launch with `-mod lowHDmain -txt`, replacing the name with your installed variant. Main and partial use `-txt` for reduced missile particles.
3. **Never extract updates over a customized mod folder.** Move or rename the existing folder first. The companion launcher refuses conflicting installations.

Optional graphics settings are described in each package’s `optimal_settings` folder. For separate game settings, consult the `savepath` field in `modinfo.json`; the Nexus instructions describe changing `../` to `./lowHD[...]`. These optional changes are not applied automatically.

After a D2R patch, `data/global/dataversionbuild.txt` may need the current game build. The author generally revises these variants after patches. The initial GitHub packages specify build **93847**.

## Shader-inclusive packages

The 2026-10-19 release preserves the author-approved installed versions. Main, filler and min contain shader `.bin` files; partial currently has none. These packages were not sourced from the older `NOSHADERS` archives. Each release includes `SHA256SUMS.txt` and `catalog.json` for verification.

## Screenshots, details and credits

See [the original lowHD Nexus page](https://www.nexusmods.com/diablo2resurrected/mods/1054?tab=description) for screenshots and further details.

Inspired by Gimli’s TinyMod, mininexus mod and numerous modders on inven. Original package credits are retained. Release preparation and companion launcher development received substantial help from ChatGPT Codex.
