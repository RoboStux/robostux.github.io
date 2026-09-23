# Changelog

All notable changes to robostux.github.io are documented here.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.1.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## v1.0.1

### Fixed
- GitHub Pages was using the legacy branch-deploy build system, which can silently stop auto-deploying with no error recorded anywhere (discovered on SeasonalOverlaysLibrary — its live site served stale content for over an hour with no visible failure). Switched to GitHub Actions-based Pages deployment (`.github/workflows/pages.yml`), making every deploy an ordinary, observable CI run instead.

## v1.0.0

### Added
- Initial GitHub Pages redirect repo for RoboStux, redirecting `robostux.github.io` to `github.com/RoboStux` — `VERSION.md`/`CHANGELOG.md`/`CONTRIBUTING.md`/`commit.sh`+`commit.bat` added, following the standard release-flow convention used across other StuxieDev projects.
