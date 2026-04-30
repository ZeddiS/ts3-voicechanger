# Changelog

All notable changes to **Voice Changer** are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.2.4] - 2026-04-30
### Changed
- All UI text translated to English
- About URL points to dedicated zeddihub-teamspeak-voicechanger repo

## [1.2.3] - 2026-04-30
### Added
- Per-preset menu items in Plugins top bar (one click = pick preset + enable)
- Compat Mode toggle for diagnosing VAD blocking

## [1.2.2] - 2026-04-30
### Fixed
- Pre-allocate scratch buffers in constructor (avoid heap allocation on audio thread)

## [1.2.1] - 2026-04-30
### Added
- VolumeBoost sanity-test preset
### Fixed
- NaN/Inf protection
- Robot uses AM instead of full ring mod
- Pitch shifter wraps gSumPhase to [-PI, PI]

## [1.2.0] - 2026-04-30
### Added
- 5 new effects: Distortion, Whisper, Telephone, Underwater, Megaphone
### Fixed
- Off preset now guaranteed to never set edited=1

## [1.0.0] - 2026-04-30
### Added
- Initial release: Helium / Chipmunk / Demon / Deep / Robot / Echo / Custom + phase-vocoder pitch shifter
