# lowHD + D2R QoL

[Restore panel backgrounds and click blocking](RESTORE-PANELS.md#english)

Diablo II: Resurrected mods by **celloboy126** on jsp, Nexus Mods and Traderie.

**[한국어 설치 및 문제 해결 안내](README.ko.md)**

## Download the mods

**Last updated: November 12, 2026.** Open the **[latest mod release](https://github.com/celloboy126/lowHD/releases/latest)** and download a ZIP under **Assets**, or use these direct links:

| Download | Purpose | Updated |
| --- | --- | --- |
| [lowHDmain.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.11.12/lowHDmain.zip) | Main performance variant | November 12, 2026 |
| [lowHDfiller.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.11.12/lowHDfiller.zip) | Filler accounts | November 10, 2026 |
| [lowHDmin.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.11.12/lowHDmin.zip) | Minimal visuals | November 12, 2026 |
| [lowHDpartial.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.11.12/lowHDpartial.zip) | More retained game visuals | November 12, 2026 |
| [QoL.zip](https://github.com/celloboy126/lowHD/releases/download/v2026.11.12/QoL.zip) | Original graphics with QoL improvements | November 10, 2026 |

Use these ZIP assets, **not GitHub's automatic source-code archives**. The [0.17.10 launcher](https://github.com/celloboy126/D2R-Multigate-Launcher/releases/latest) bundles the same verified mod contents and offers installation tools.

## November 12 refresh

lowHDpartial ships nine empty cinematic video files and seven empty companion audio files. The optional extracted-data copy preserves these files, avoiding approximately 2.15 GiB of duplicate media. The lowHD shaders and in-game audio assets are unchanged by this edit. Use the lowest graphics preset with lowHDpartial. The bundle also includes current main and partial Catacombs waypoint files and the min menu/layout fixes.

## Visual badges and this refresh

All five variants include discreet gold screen/panel badges and paired rectangular player-count markers for the launcher's visual recognition and parking. Older/unmodified setups retain the launcher's legacy recognition fallbacks. Restart D2R after updating to reload cached layouts and textures.

Main includes conservative 128×128 native-mip hair-control textures. Filler now uses the same HUD transparency as main, exposing the existing count markers. The launcher still performs screen-based recognition without game-memory access or injection.

## What is included

lowHD reduces visual content to lower resource use, particularly for multiple D2R accounts. Main, filler, min and the new partial package include the author-supplied shader `.bin` files; QoL contains no shader binaries. These are the current shader-inclusive packages, not older NOSHADERS archives.

QoL preserves normal audio and cinematics and the original HD graphics apart from its targeted visual improvements: a gentler Thunderstorm effect without the full-screen flash, increased unique-monster saturation, and altered sprites for features such as transparent panels. It includes player metadata, fast exit to lobby, transparent click-through panels, make/join controls, automatic lobby game-name focus and full arrow-key game-menu navigation. The fresh mods also accept **Enter** to open the lobby from online character selection.

## Installation

1. Download a variant from the links above.
2. Extract it into D2R's `mods` folder. For example: `mods/lowHDmain/lowHDmain.mpq/modinfo.json`.
3. Launch with `-mod lowHDmain`, replacing the name for another variant.

Optional: append **`-ns`** to prevent sound from loading, particularly for filler/min accounts. Main and partial also support **`-txt`** for reduced missile particles.

Preserve custom edits: move or rename an existing mod folder before manually extracting an update. In the launcher, disable automatic bundled-mod replacement if you maintain your own changes. Its normal fresh-install action refuses a conflicting name; its explicitly permitted update action can replace the installed bundled mods after games close.

Optional low-graphics presets are in each lowHD package's `optimal_settings` folder. The launcher can apply low or standard graphics/save-path settings and import movement keybindings; existing saved graphics/key files are preserved by the creation-only import. See the [original Nexus instructions](https://www.nexusmods.com/diablo2resurrected/mods/1054?tab=description) for manual setup and screenshots. After a game patch, download the author's compatible package; changing `data/global/dataversionbuild.txt` alone does not establish compatibility.

## Verification and download counts

Each release includes **catalog.json** and **SHA256SUMS.txt**. Archive paths satisfy the launcher's strict installer, and every file is verified against the reviewed mod folders. The standalone ZIPs are byte-for-byte identical to the packages embedded in launcher 0.17.10.

GitHub records each release asset's `download_count` in the [public release API](https://api.github.com/repos/celloboy126/lowHD/releases?per_page=100). These are download requests, not unique people or installations. Repeated downloads count again; installing an already bundled mod does not download another GitHub asset. No country tracking or launcher telemetry is added for these counts.

## Credits and contact

Original credits inside the packages are retained. Inspired by Gimli's TinyMod, mininexus mod, and numerous modders on Inven. By celloboy126, with Codex.

[Launcher and documentation](https://github.com/celloboy126/D2R-Multigate-Launcher) · [Discord: celloboy126](https://discord.com/users/754143383978508379)

## Optional extracted assets for partial

The 0.17.0 launcher can copy missing extracted assets into **lowHDpartial only**. Install partial, extract game data using the launcher, then use **Copy extracted data into lowHDpartial** under lowHD / QoL mods. Existing files, zero-byte overrides and the partial build marker are preserved. Keep using `-mod lowHDpartial`. Expect substantial additional disk space; the confirmation shows the actual amount. Mod updates replace the expanded folder, so refresh extracted data and repeat the copy afterward.
