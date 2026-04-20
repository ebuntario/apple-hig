# Changelog

All notable changes to `apple-hig` will be documented here. Format:
[Keep a Changelog](https://keepachangelog.com/en/1.1.0/). Versioning:
[SemVer](https://semver.org/). Each authoring batch maps to a minor release.

## [0.2.0] — 2026-04-20

Foundations complete + deep platform references for iOS and macOS. Every file
cites its source on developer.apple.com and follows the shared template
(What / When / Platform differences / Sizing / Accessibility / Common mistakes
/ SwiftUI / UIKit or AppKit / See also).

### Added — Foundations (8 files)

- `foundations/accessibility.md` — hit-target and Dynamic Type tables per
  platform, WCAG contrast minimums, VoiceOver rules, Reduce Motion
  alternatives, Voice Control / Full Keyboard Access / Switch Control /
  Assistive Access.
- `foundations/typography.md` — SF Pro / SF Compact / New York, the text-style
  hierarchy, default and minimum point sizes per platform, macOS built-in text
  styles, tvOS built-in text styles, Dynamic Type rules, custom-font
  requirements.
- `foundations/color.md` — 12 system colors, 6 system grays, iOS and macOS
  semantic color catalogs, Liquid Glass tinting guidance, inclusive-color
  rules, sRGB vs Display P3 management.
- `foundations/dark-mode.md` — base vs elevated backgrounds on iOS/iPadOS,
  desktop tinting on macOS, contrast floors in dark appearance, asset-catalog
  practice, why an app-specific appearance toggle is wrong.
- `foundations/layout.md` — hierarchy, adaptability, safe areas and guides,
  per-platform layout rules, iPhone / iPad / Apple Watch dimension tables, and
  iOS / iPadOS size classes.
- `foundations/sf-symbols.md` — rendering modes, gradients, variable color,
  weights and scales, design variants, the full animation vocabulary, custom
  symbols and annotation.
- `foundations/materials.md` — Liquid Glass regular vs clear variants,
  standard materials (ultra-thin / thin / regular / thick), vibrancy levels,
  per-platform differences including the visionOS glass material.
- `foundations/motion.md` — purposeful motion, Reduce Motion alternatives,
  visionOS comfort rules (peripheral motion, 0.2 Hz oscillation, no
  world-rotation).

### Added — Platforms (2 deep files)

- `platforms/ios.md` — device traits, system features to integrate (Dynamic
  Island, Live Activities, widgets, Action button, App Clips, Shortcuts),
  navigation paradigm, layout rules, typography, color and materials, touch
  and gestures, feedback via haptics, modality used sparingly, writing style,
  common mistakes, a full SwiftUI inbox screen, and a UIKit equivalent.
- `platforms/macos.md` — device traits, the big Mac idioms (menu bar is
  authoritative), windowing rules, menu bar / toolbar / sidebar / split view
  structure, keyboard and pointer expectations, layout rules, typography
  (with the correct point sizes for macOS — no Dynamic Type), color and
  materials, Settings scene, writing conventions, Mac Catalyst notes, common
  mistakes, a full SwiftUI three-column app with menu commands and a Settings
  scene, and an AppKit sketch.

### Pending

- Core components: bars, buttons, lists-and-tables, sheets-and-popovers,
  text-inputs, pickers-and-menus (batch 4).
- Core patterns: navigation, modality, settings, search, onboarding, loading,
  feedback (batch 5).
- Lighter platform files: iPadOS, watchOS, tvOS, visionOS (batch 8).
- Checklists refresh, technologies, inputs.

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
