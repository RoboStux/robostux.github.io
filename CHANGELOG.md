# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Date Versioning](https://datevers.ing) since v26.10.23 (`YY.MM.DD`, the UTC release date, with `-1`, `-2`… for later releases the same day); earlier releases used [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v26.11.06-1

### Added

- `.github/workflows/ci.yml`, which runs `tests/version.sh` on every push to `main` and `test` and on every pull request

### Changed

- Work happens on the new `test` branch and reaches `main` only through a pull request, reviewed and merged by Leo; releases are committed and tagged on `test`. `CONTRIBUTING.md` has a Branches section, the README's Versioning section says so, and `commit.sh`/`commit.bat` say to push `test`

## v26.11.06

### Changed

- `README.md` now describes this repository (the robostux.github.io redirect to github.com/RoboStux, published by the Pages workflow) instead of the generic redirect template it was made from, which told readers to fork it and replace `example.com`, and claimed it preserved URL paths, which it doesn't
- `README.md` and `CONTRIBUTING.md` show the RoboStux logo instead of the StuxieDev one, and the README's license line says (C) StuxieDev, and its footer matches the organisation profile's

## v26.10.23

### Added

- `tests/version.sh`, which checks that `VERSION.md` is a valid Date Version, a real calendar date not in the future, and the same as the newest entry in this changelog

### Changed

- Switched from Semantic Versioning to [Date Versioning](https://datevers.ing): releases are numbered by their UTC release date as `YY.MM.DD`, with `-1`, `-2`… for later releases the same day. This release follows v1.0.0
- `commit.sh` and `commit.bat` refuse a `VERSION.md` that isn't a valid Date Version or is dated in the future (UTC), and warn when it's dated before today
- `README.md` and `CONTRIBUTING.md` describe Date Versioning and the release steps

## [1.0.0] - 2026-09-29

The first release under a fresh version history. Earlier versions and their tags have been retired.

### Added
- A GitHub Pages redirect from `robostux.github.io` to `github.com/RoboStux`, deployed with the Pages Actions workflow
- `commit.sh`/`commit.bat` release scripts that read `VERSION.md` and tag `vX.Y.Z`
