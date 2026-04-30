# Voice Changer

[![Latest Release](https://img.shields.io/github/v/release/ZeddiS/zeddihub-teamspeak-voicechanger)](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger/releases)
[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](LICENSE)

Real-time DSP effects on outgoing microphone audio. Helium / Demon / Robot / Echo / Telephone / Underwater / Megaphone / Distortion / Whisper / Custom pitch slider. Per-preset menu in Plugins top bar.

Part of the [**ZeddiHub TeamSpeak Addons**](https://github.com/ZeddiS/zeddihub-teamspeak-addons) collection.

---

## Instalace

### A) Installer (.exe) - doporuceny zpusob

Stahni a spust z [Releases](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger/releases/latest):

**`VoiceChanger-Setup-v1.2.3.exe`**

Wizard:
1. Detekuje tvou TS3 verzi a vybere spravnou API DLL (23 / 24 / 25 / 26)
2. Detekuje bezici TS3 a nabidne uzavreni
3. Nainstaluje DLL do `%APPDATA%\TS3Client\plugins\` (per-user, bez admin prav)
4. Zaregistruje uninstaller v Add/Remove Programs

### B) Manualni instalace (.zip)

Vyber zip podle sve TS3 verze v [Releases](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger/releases/latest):

| TS3 client | API | Stahni |
|---|---|---|
| 3.5.0 | 23 | `VoiceChanger-v1.2.3-TS3-3.5.0-api23.zip` |
| 3.5.1 - 3.5.5 | 24 | `VoiceChanger-v1.2.3-TS3-3.5.1-3.5.5-api24.zip` |
| **3.5.6** | **25** | **`VoiceChanger-v1.2.3-TS3-3.5.6-api25.zip`** |
| 3.6.x+ | 26 | `VoiceChanger-v1.2.3-TS3-3.6+-api26.zip` |

Rozbal zip, zkopiruj DLL do `%APPDATA%\TS3Client\plugins\`, a v TS3 -> Settings -> Plugins -> Reload All -> zaskrtni Enabled.

## Build ze zdrojaku

```powershell
# 1. Pozadavky
py -m pip install aqtinstall
py -m aqt install-qt windows desktop 5.12.12 win64_msvc2017_64 -O C:\Qt --archives qtbase
git clone https://github.com/TeamSpeak-Systems/ts3client-pluginsdk.git ts3sdk_clone
Move-Item ts3sdk_clone\include ts3sdk\include

# 2. Build (napr. pro TS3 3.5.6 = API 25)
cmake -S . -B build_api25 -G "Visual Studio 17 2022" -A x64 `
      -DCMAKE_PREFIX_PATH="C:\Qt\5.12.12\msvc2017_64"
cmake --build build_api25 --config Release
```

Output: `build_api25\Release\voicechanger_api25_win64.dll`

## Changelog

Viz [CHANGELOG.md](CHANGELOG.md).

## License

MIT - viz [LICENSE](LICENSE).

---

## Links

- **Web**: [zeddihub.eu](https://zeddihub.eu)
- **ZeddiHub Tools**: [zeddihub.eu/tools](https://zeddihub.eu/tools/)
- **Author**: [zeddis.xyz](https://zeddis.xyz)
- **Collection**: [zeddihub-teamspeak-addons](https://github.com/ZeddiS/zeddihub-teamspeak-addons)
- **Sister plugins**: [pokebot](https://github.com/ZeddiS/zeddihub-teamspeak-pokebot) | [follow](https://github.com/ZeddiS/zeddihub-teamspeak-follow) | [movespam](https://github.com/ZeddiS/zeddihub-teamspeak-movespam) | [voicechanger](https://github.com/ZeddiS/zeddihub-teamspeak-voicechanger) | [autoreconnect](https://github.com/ZeddiS/zeddihub-teamspeak-autoreconnect) | [greetingbot](https://github.com/ZeddiS/zeddihub-teamspeak-greetingbot)

---

(C) 2026 [ZeddiHub.eu](https://zeddihub.eu) - zeddis.xyz
