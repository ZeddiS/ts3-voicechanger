# Voice Changer

[![Release](https://img.shields.io/github/v/release/ZeddiS/zeddihub-teamspeak-voicechanger)](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Real-time DSP voice effects for outgoing TeamSpeak 3 microphone audio.

**Standalone plugin** -- not part of the curated [ZeddiHub TeamSpeak Addons](https://github.com/ZeddiS/zeddihub-teamspeak-addons) collection (Voice Changer is experimental and may not work on all setups).

## Installation

Latest release: **[v1.2.5](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger/releases/latest)**

**Recommended:** Download oicechanger-v1.2.5-TS3-<your-version>-apiNN.ts3_plugin and double-click. TS3 native install dialog opens.

**Manual:** Download oicechanger_apiNN_win64.dll and copy to %APPDATA%\TS3Client\plugins\.

| TS3 client | API |
|---|---|
| 3.5.0 | 23 |
| 3.5.1 - 3.5.5 | 24 |
| **3.5.6** | 25 |
| 3.6.x and newer | 26 |

## Voice presets

Pitch shifters: Helium, Chipmunk, Deep, Demon, Custom (-12..+12 semitones)
Effects: Robot (AM), Echo, Distortion, Whisper, Telephone, Underwater, Megaphone
Diagnostic: Volume Boost (1.5x gain), Bypass (no-op + edited flag), Off

## Known issue (v1.2.5)

On some TS3 client setups, setting edited=1 in the audio callback breaks Voice Activity Detection (VAD) -- talk indicator stops lighting even though mic input is detected.

**Workaround:** Compat Mode is now ON by default (does NOT set edited=1). With Compat Mode ON:
- Mic and VAD work normally
- Voice modifications may NOT transmit (TS3 might use original samples)

Use the **Bypass** preset to test if your TS3 setup tolerates the edited flag. If Bypass keeps your mic working with Compat Mode OFF, voice changing should work for you. If it breaks even with Bypass, your setup requires Compat Mode permanently.

**Recommended:** use TS3 in Push-to-Talk mode while Voice Changer is active.

## Theme

Plugin dialogs use TS3 client's native theme (no custom Discord-style overrides).

## Source code

Source lives in [zeddihub-teamspeak-addons](https://github.com/ZeddiS/zeddihub-teamspeak-addons), folder VoiceChanger/.

## License

MIT -- see [LICENSE](LICENSE).

---

## Links

- **ZeddiHub web**: https://zeddihub.eu
- **ZeddiHub Tools**: https://zeddihub.eu/tools/
- **Author**: https://zeddis.xyz
- **Curated collection**: [zeddihub-teamspeak-addons](https://github.com/ZeddiS/zeddihub-teamspeak-addons) (4 plugins: PokeBot, Follow, MoveSpam, Soundboard)

(C) 2026 [ZeddiHub.eu](https://zeddihub.eu) -- zeddis.xyz
