# Changelog

All notable changes to the Data Editor For Mainframe extension are documented in this file.

## [1.1.3] - 2026-08-04

#### Changed
 - End of support for File Master Plus version 10
 - Readme update

#### Fixed
- Miscellaneous bug fixes

## [1.1.2] - 2026-03-18

### Fixed

- Special character encoding in document URI
- Telemetry
- Opening PDS members from filtered Zowe Explorer tree

## [1.1.1] - 2025-11-24

### Fixed

- Applying selection criteria in character mode now works correctly instead of displaying an error message.
- Stale cached records that do not match the active selection criteria are no longer displayed in single record mode.

## [1.1.0] - 2025-07-31

#### Changed

- Readme update

#### Added

- Option to connect via Zowe API Mediation Layer.
- MFA and SSO enabled via Zowe Explorer.

#### Fixed

- HTTPS support for Server URL.

## [1.0.0] - 2022-04-20

#### Changed

- Remove Zowe Explorer dependency.
- Highlight protected field which can't be edited.
- Enhance UI.
- Enhance edit support.

#### Added

- Ability to open data set in edit mode.
- Browse and edit support for sequential and partitioned data sets.
- Ability to show DSN Info.
- Ability to insert new records into a PDS member, a sequential file or a VSAM KSDS.
- Telemetry events recording.

#### Fixed

- Lock input on dirty state.

## [0.5.1] - 2021-12-23

#### Fixed

- Enable hex edit for protected fields in Character mode.
- Enable selection criteria apply button when no records found in previous search.

## [0.5.0] - 2021-12-22

#### Added

- Edit functionality

#### Changed

- Hexadecimal mode in Character view is now enabled by default
- Readme update

## [0.4.0] - 2021-08-20

- Initial release
