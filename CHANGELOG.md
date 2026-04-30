# Changelog

All notable changes to **Voice Changer** are documented here.
Format follows [Keep a Changelog](https://keepachangelog.com/en/1.1.0/).

## [1.2.3] - 2026-04-30
### Added
- Per-preset menu items in Plugins top bar (one click = pick preset + enable)
- Compat Mode toggle - when ON, plugin does not set edited=1 (mic stays working but voice changes do not transmit; useful for diagnosing VAD blocking)

## [1.2.2] - 2026-04-30
### Fixed
- Pre-allocate scratch buffers in constructor (avoid heap allocation on audio thread)

## [1.2.1] - 2026-04-30
### Added
- VolumeBoost sanity-test preset (1.5x gain, no other DSP)
### Fixed
- NaN/Inf protection in floatToInt16
- Robot uses AM (amplitude modulation) instead of full ring mod (no zero-cross silence)
- Distortion: removed post-clip 0.7x attenuation
- Whisper: less aggressive attenuation (0.4x instead of 0.15x)
- Pitch shifter wraps gSumPhase to [-PI, PI] (precision drift fix)

## [1.2.0] - 2026-04-30
### Added
- 5 new effects: Distortion, Whisper, Telephone, Underwater, Megaphone
- Settings dialog reorganized with Pitch / Effects section dividers
### Fixed
- Off preset now guaranteed to never set edited=1

## [1.0.0] - 2026-04-30
### Added
- Initial release: Helium / Chipmunk / Demon / Deep / Robot / Echo / Custom + phase-vocoder pitch shifter
