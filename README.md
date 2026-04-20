# apple-hig

A Claude Code skill that makes Claude actually follow Apple's [Human Interface Guidelines](https://developer.apple.com/design/human-interface-guidelines/) when you're building for iOS, iPadOS, macOS, watchOS, tvOS, or visionOS — instead of producing generic "Apple-ish" output.

Works with **SwiftUI**, **UIKit**, **AppKit**, and web/Figma mockups that need to feel Apple-native.

> Status: **0.1.0 — scaffold.** Skill content is being authored. Triggers and structure are in place; reference files are being filled in from the live HIG. See [`CHANGELOG.md`](./CHANGELOG.md).

## What it does

When you mention building something for an Apple platform, this skill kicks in automatically and:

1. **Asks a couple of targeting questions first** (platform, framework, what you're actually building) — so the answer fits your context, not a generic mold.
2. **Loads only the reference files that matter** for your task — progressive disclosure, no context bloat.
3. **Applies the non-negotiables** every time: semantic colors, Dynamic Type, SF Symbols, ≥44pt touch targets, VoiceOver labels, Reduce Motion, platform-correct navigation.
4. **Cites the live HIG** at the top of every reference file so you can verify.

## Install

Paste this into Claude Code:

```bash
git clone --single-branch --depth 1 https://github.com/ebuntario/apple-hig.git ~/.claude/skills/apple-hig && cd ~/.claude/skills/apple-hig && ./setup
```

Then start a new Claude Code session. Ask about an Apple-platform UI and the skill auto-triggers.

## Update

```bash
cd ~/.claude/skills/apple-hig && git pull
```

## Uninstall

```bash
~/.claude/skills/apple-hig/bin/apple-hig-uninstall
```

Or just `rm -rf ~/.claude/skills/apple-hig`.

## What it covers

| Area | Depth |
|---|---|
| iOS / iPhone | Deep |
| macOS | Deep |
| iPadOS | Solid |
| watchOS | Solid |
| tvOS | Solid |
| visionOS | Solid |
| SwiftUI snippets | Primary |
| UIKit / AppKit snippets | Secondary |
| Web / Figma native-feel | Notes where relevant |

Reference tree mirrors the HIG: `foundations/`, `patterns/`, `components/`, `inputs/`, `platforms/`, `technologies/`. See the [full structure](./SKILL.md).

## How it differs from similar skill packs

- **No CLAUDE.md injection.** `./setup` does not edit your global config. The skill is discovered by the Claude Code harness on its own. If you want it imported into `CLAUDE.md` explicitly, run `./setup --inject-claudemd`.
- **Question-first.** The skill asks before generating, because "an iOS app" and "a macOS menu bar app" need very different answers.
- **Cited, not invented.** Every reference file starts with the HIG URL it's sourced from. If the HIG is silent on something, the file says so and labels the default.

## Contributing

PRs welcome — especially for:
- HIG updates after a WWDC release.
- Missing component/pattern files.
- Better SwiftUI/UIKit/AppKit snippets.

Keep snippets idiomatic for the current deployment targets listed in each file. Don't paraphrase large blocks of Apple's prose; short quotes + citations only.

## License

[MIT](./LICENSE)
