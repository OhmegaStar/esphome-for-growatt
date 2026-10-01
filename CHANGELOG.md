# Changelog

Notable changes to the Growatt ESPHome configurations are recorded here.
Versions follow Semantic Versioning.

## [1.1.1] - 2026-10-01

### Changed
- added changelog, and updated release tooling accordingly (1d45754)
## [1.1.0] - 2026-10-01

### Changed
- Replaced deprecated per-entity `skip_updates` settings with same-address Modbus controllers polling at 15, 60, and 300 seconds in the SPH and MOD configurations.
- Consolidated fast polling under the `update_fast` substitution.
- Required encrypted OTA updates, reusing each configuration's API encryption key instead of a separate OTA password.
- Migrated SPH one-shot writes and both inverter fault-code parsers to current ESPHome Modbus APIs.

## [1.0.0] - 2026-10-01

### Added
- Initial release of the Growatt ESPHome configurations, including confirmed support for the SPH10000TL3-BH-UP and MOD10000TL3-X.
- Register-based inverter monitoring and Home Assistant controls, including SPH Battery First timeslot settings and operating-mode controls.
- GitHub release workflow and PowerShell helper for versioned releases and README updates.

### Changed
- Updated the primary inverter configurations for ESPHome 2026.8 Modbus changes and the ESP-IDF framework.
- Exposed inverter priority through read-only register 118 and removed the unsupported register 1044 select option.

### Fixed
- Corrected Modbus readings and Battery SoC device/state metadata.
- Fixed race conditions when updating Battery First timeslot start and end values, and improved duplicate-command handling.
- Updated select state access to use `current_option()`.