# Changelog
All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.3] - 2023-04-08
### Added
- an optional input `skip-save` that allows to skip saving the cache
- cache related outputs: `cache-hit`, `cache-primary-key`, `cache-matched-key`

### Fixed
- restore usage of official actions/cache action(s)

## [1.1.2] - 2023-03-03
### Fixed
- use sed instead of grep on macos
- use $HOME instead of realpath because the later is not available on macos

## [1.1.1] - 2023-03-03
### Fixed
- how sccache is downloaded on macos

## [1.1.0] - 2022-11-14
### Changed
- updated the default version of sccache to v0.3.1

## [1.0.1] - 2022-11-14
### Changed
- do not require GITHUB_TOKEN to be set for the action

### Fixed
- do not use deprecated GitHub expressions (set-output)

## [1.0.0] - 2022-04-11
### Added
- action that enables Rust [sccache](https://github.com/mozilla/sccache)
