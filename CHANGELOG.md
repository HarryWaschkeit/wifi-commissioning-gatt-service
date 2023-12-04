# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [0.3.9] Q4 2023
- fixed cargo clippy warning

## [0.3.8] Q4 2023
- bumped toolchain to 1.74.0

## [0.3.7] Q3 2023
- bumped toolchain to 1.65.0

## [0.3.6] Q2 2023
- extended readme by information to open source component

## [0.3.5] Q2 2023
- fixed dependency versions in Cargo.lock file

## [0.3.4] Q2 2023
- fixed bug that prevented changing wifi connections

## [0.3.3] Q1 2023
- fixed cargo clippy warnings

## [0.3.2] Q1 2023
- introduced rust-toolchain.toml to enforce same rust version as used by kirkstone

## [0.3.1] Q1 2023
- updated tokio to 1.23 in order to fix cargo audit warning

## [0.3.0] Q4 2022
- renamed from ICS-DeviceManagement to omnect github orga

## [0.2.6] Q3 2022
- systemd: start service as user `wifi-commissioning-gatt`
  (fixes systemd warning: "Special user nobody configured, this is not safe!")

## [0.2.5] Q3 2022
- moved systemd service file from meta-ics-dm

## [0.2.4] Q3 2022
- fixed 32bit builds by updating `wpactrl` to 0.5.*
- updated all dependencies via `cargo update`

## [0.2.3] Q3 2022
- updated dependencies (especially bluer)

## [0.2.2] Q2 2022
- add client/web_ble.html in [README](./README.md)

## [0.2.1] Q1 2022
- fixed multiple cargo audit warnings by updating dependencies

## [0.2.0] Q1 2022
- added optional feature `systemd` (see [README](./README.md))
- clap: use version and author from Cargo.toml

## [0.1.5] Q1 2022
- Cargo.toml: added SPDX license expression
- restructured Changelog.txt -> Changelog.md
- renamed license files

## [0.1.4]
Added authentication feature (device will deny read/write unless authentication key characteristic has been written with the correct value first.
Key is Sha3_256 hash of the device id.
Device Id and wlan interface can be specified on the cmdline.

## [0.1.3]
Remove wifiscanner dependency since it does not produce correct JSON format for non-ascii unicode.
Instead use WpaCtrl for scanning, which also makes running the service as non-root possible.

## [0.1.2]
Report errors for wpa_supplicant interaction (previously errors were ignored).
Add retry for connect to bluetooth adapter on startup (previously the service paniced).

## [0.1.1]
Refactoring scan and connect

## [0.1.0]
First release