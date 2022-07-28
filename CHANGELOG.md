# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [0.4.1] - 2023-07-25

### Added

- Changelog
- Example of usage to README

### Changed

- Introduction in README

## [0.4.0] - 2023-07-25

### Added

- `Base64to16Converter.convert_json_from_filename` method
- `Base64to16Converter.convert_json_from_fp` method

### Changed

- `json_file` command line option is now optional (standard input is used if this option is absent)

### Deprecated

- `Base64to16Converter.convert_json` method (use `convert_json_from_filename` instead)

## [0.3.0] - 2022-07-20

### Added

- `Base64to16Converter` class (fully documented)
- `-x` command line option for removing `0x` prefix on hexadecimals
- `-k` command line option for also converting dictionary keys to hexadecimal

### Changed

- Does not throw `binascii.Error` when string that ends with `=` cannot be converted from Base64 to hexadecimal (simply keeps string as-is instead)

### Removed

- `base64_to_hex` function (moved to `Base64to16Converter.convert_string`)
- `traverse_data` function (moved to `Base64to16Converter.convert_data`)
- `process_json` function (moved to `Base64to16Converter.convert_json`)

## [0.2.0] - 2022-07-12

### Fixed

- Updated PyPI image to reflect actual version

## [0.1.0] - 2022-07-12

[Unreleased]: https://github.com/guidanoli/base64-to-hex-converter/compare/v0.4.1...HEAD
[0.4.1]: https://github.com/guidanoli/base64-to-hex-converter/compare/v0.4.0...v0.4.1
[0.4.0]: https://github.com/guidanoli/base64-to-hex-converter/compare/v0.3.0...v0.4.0
[0.3.0]: https://github.com/guidanoli/base64-to-hex-converter/compare/v0.2.0...v0.3.0
[0.2.0]: https://github.com/guidanoli/base64-to-hex-converter/compare/v0.1.0...v0.2.0
[0.1.0]: https://github.com/guidanoli/base64-to-hex-converter/releases/tag/v0.1.0
