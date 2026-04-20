# Changelog

All notable changes to `apple-hig` will be documented here. Format:
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Versioning:
[SemVer](https://semver.org/).

## [0.1.0] — 2026-04-20

Initial scaffold. Skill triggers, structure, and install flow are in place.
Reference file content is being authored from the live HIG.

### Added

- `SKILL.md` with trigger-heavy frontmatter, Phase 0 question flow, decision
  tree, core non-negotiables, common mistakes, and final review checklist.
- Reference directory tree:
  `references/{foundations,patterns,components,inputs,platforms,technologies}`.
- Checklist stubs under `assets/checklists/`.
- `setup` script (idempotent, no user-config edits by default).
- `bin/apple-hig-uninstall`.
- MIT license.
- GitHub Actions workflow scaffold (manual trigger only at this stage).

### Pending

- Authoring of ~60 reference files against the live HIG.
- Depth pass on iOS and macOS (SwiftUI + UIKit/AppKit snippets).
- Populated pre-submission and accessibility review checklists.
