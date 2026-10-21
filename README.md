# lowHD + D2R QoL

Diablo II: Resurrected performance and quality-of-life mods by **celloboy126** on jsp, Nexus Mods and Traderie.

lowHD reduces visual content to help lower memory use and improve performance when running D2R, especially multiple accounts. This repository distributes four lowHD variants and QoL, which retains the original graphics while adding the QoL controls from lowHDmin. Shader binaries are included in the lowHD variants where supplied. Choose a variant below or browse [Releases](https://github.com/celloboy126/lowHD/releases).

| Download | Variant |
| --- | --- |
| [lowHDmain.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.10.19/lowHDmain.zip) | Main |
| [lowHDfiller.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.10.19/lowHDfiller.zip) | Filler |
| [lowHDmin.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.10.19/lowHDmin.zip) | Min |
| [lowHDpartial.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.10.19/lowHDpartial.zip) | Partial |
| [QoL.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.10.20-QoL/QoL.zip) | Original graphics with QoL |

QoL preserves normal audio and cinematics, adds a gentler Thunderstorm effect without a full-screen flash and increased unique-monster saturation, and includes persistent other-player information (level, name, area), fast exit to lobby, transparent click-through panels, in-game make/join, automatic game-name focus in the lobby, and full arrow-key game-menu navigation. These controls support the default Make/Join workflow in **D2R Multigate Launcher**, currently in development.

## Download counts

GitHub counts downloads of each release asset. These are download requests, not unique people or mod installations. Repeated downloads count again, and bundled offline mod installs do not download a separate GitHub asset. Automatic source-code ZIP downloads are not the mod packages.

[![lowHDmain downloads](https://img.shields.io/github/downloads/celloboy126/lowHD/lowHDmain.zip?label=lowHDmain)](https://github.com/celloboy126/lowHD/releases)
[![lowHDfiller downloads](https://img.shields.io/github/downloads/celloboy126/lowHD/lowHDfiller.zip?label=lowHDfiller)](https://github.com/celloboy126/lowHD/releases)
[![lowHDmin downloads](https://img.shields.io/github/downloads/celloboy126/lowHD/lowHDmin.zip?label=lowHDmin)](https://github.com/celloboy126/lowHD/releases)
[![lowHDpartial downloads](https://img.shields.io/github/downloads/celloboy126/lowHD/lowHDpartial.zip?label=lowHDpartial)](https://github.com/celloboy126/lowHD/releases)
[![QoL downloads](https://img.shields.io/github/downloads/celloboy126/lowHD/QoL.zip?label=QoL)](https://github.com/celloboy126/lowHD/releases)

The [public release API](https://api.github.com/repos/celloboy126/lowHD/releases?per_page=100) exposes each asset's `download_count`. Only download counts are used; no country tracking is planned. No telemetry is added to the launcher for these counts.

## Installation

1. Download one variant from Releases. Use the ZIP assets rather than GitHub's automatic source-code ZIP.
2. Extract into your D2R `mods` folder. For example, the result should include `mods/lowHDmain/lowHDmain.mpq/modinfo.json`.
3. Launch D2R with `-mod lowHDmain -txt`, replacing `lowHDmain` with the installed variant name. Main and partial use `-txt` for reduced missile particles.

**Preserve customized installations:** do not extract updates over an existing mod folder. Move or rename your existing folder first. The companion launcher refuses a conflicting installation instead of overwriting it.

Optional low-graphics settings are described in each package's `optimal_settings` folder. To keep separate game settings, see the `savepath` field in `modinfo.json`: the Nexus instructions describe changing `../` to `./lowHD[...]`. These changes are optional and are not applied automatically.

After a D2R patch, the mod's `data/global/dataversionbuild.txt` may need updating to the current game build. The author generally revises these variants after patches; download the latest compatible release rather than overwriting your own adjustments blindly.

## Shader-inclusive packages

The 2026-10-19 release preserves the author-approved installed versions. Main, filler and min include shader `.bin` files; partial currently contains none. These are the shader-inclusive packages, not the older `NOSHADERS` archives. `SHA256SUMS.txt` and `catalog.json` accompany each release for verification.

## Details, screenshots and credits

See [the original lowHD Nexus page](https://www.nexusmods.com/diablo2resurrected/mods/1054?tab=description) for screenshots and more information.

Inspired by Gimli's TinyMod, mininexus mod, and numerous modders on inven. All original credits within the packages are retained. Release preparation and companion launcher development by celloboy126, with Codex.
