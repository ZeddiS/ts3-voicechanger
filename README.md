# Voice Changer

[![Latest Release](https://img.shields.io/github/v/release/ZeddiS/zeddihub-teamspeak-voicechanger)](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Real-time DSP effects on outgoing microphone audio.

Helium / Chipmunk / Demon / Deep / Custom pitch (phase-vocoder), Robot (AM modulation), Echo (delay), Distortion (raspy/guttural), Whisper (breathy), Telephone (300-3400 Hz bandpass), Underwater (muffled + reverb), Megaphone (PA-system distortion + bandpass), Volume Boost (sanity test). Each preset has a one-click menu item under Plugins -> Voice Changer.

Part of the [**ZeddiHub TeamSpeak Addons**](https://github.com/ZeddiS/zeddihub-teamspeak-addons) collection.

---

## Installation

All download files are in **[Releases](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger/releases/latest)**.

### Option A: Installer (.exe) -- recommended

Download and run **`VoiceChanger-Setup-v1.2.4.exe`**

The wizard:
1. Detects your TeamSpeak 3 version and selects the correct API DLL (23 / 24 / 25 / 26)
2. Detects running TS3 and offers to close it (DLL would otherwise be locked)
3. Installs the DLL to `%APPDATA%\TS3Client\plugins\` (per-user, no admin needed)
4. Registers an uninstaller in Add/Remove Programs

### Option B: Manual (.dll)

Download the raw DLL matching your TS3 client version:

| TS3 client | Plugin API | File |
|---|---|---|
| 3.5.0 | 23 | `voicechanger_api23_win64.dll` |
| 3.5.1 - 3.5.5 | 24 | `voicechanger_api24_win64.dll` |
| **3.5.6** | **25** | **`voicechanger_api25_win64.dll`** |
| 3.6.x and newer | 26 | `voicechanger_api26_win64.dll` |

Copy the DLL to `%APPDATA%\TS3Client\plugins\`, then in TS3 go to **Settings -> Plugins -> Reload All -> tick Enabled**.

If TS3 reports 'API version not compatible', you have the wrong file -- try a different API number.

## Source code

Source code lives in the [**collection repo**](https://github.com/ZeddiS/zeddihub-teamspeak-addons), folder `VoiceChanger/`. Build instructions and CMake configuration are there.

## Changelog

See [CHANGELOG.md](CHANGELOG.md).

## License

MIT -- see [LICENSE](LICENSE).

---

## Links

- :house: **ZeddiHub web**: https://zeddihub.eu
- :wrench: **ZeddiHub Tools**: https://zeddihub.eu/tools/
- :busts_in_silhouette: **Author**: https://zeddis.xyz
- :file_folder: **Collection**: [zeddihub-teamspeak-addons](https://github.com/ZeddiS/zeddihub-teamspeak-addons)

**Sister plugins:** [Poke Bot](https://github.com/ZeddiS/zeddihub-teamspeak-pokebot) | [Follow](https://github.com/ZeddiS/zeddihub-teamspeak-follow) | [MoveSpam](https://github.com/ZeddiS/zeddihub-teamspeak-movespam) | [Voice Changer](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger) | [AutoReconnect](https://github.com/ZeddiS/zeddihub-teamspeak-autoreconnect) | [Greeting Bot](https://github.com/ZeddiS/zeddihub-teamspeak-greetingbot)

---

(C) 2026 [ZeddiHub.eu](https://zeddihub.eu) -- zeddis.xyz
