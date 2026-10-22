# Editor Width Slider (unlimited)

Fork of [MugishoMp/obsidian-editor-width-slider](https://github.com/MugishoMp/obsidian-editor-width-slider) (MIT). This repository holds only the built plugin: `main.js` and `manifest.json`.

## What changed

The slider in the status bar now runs from 700px (slider at 0) to the full window width (slider at 100). In the original the range ended at 1700px, so on wide screens the margins never went away.

The formula, in the two CSS variables the plugin sets:

```
calc(700px + <slider> * (100vw - 700px) / 100)
```

The plugin id is unchanged (`editor-width-slider`), so this build replaces the original in place and keeps the saved slider position.

## Requirements

Obsidian applies `--line-width` and `--file-line-width` only when "Readable line length" is on (Settings → Editor). Keep it enabled.

## Installation

1. Download `main.js` and `manifest.json` from this repository.
2. Put them in `<vault>/.obsidian/plugins/editor-width-slider/`, replacing the original files.
3. Restart Obsidian and enable the plugin in Settings → Community plugins.

## Usage

Drag the slider in the status bar. Clicking the number next to it resets the width.

A single note can have its own width: add `editor-width` (0 to 100) to the note's YAML frontmatter.

```yaml
---
editor-width: 75
---
```

## Source

The source code is in the history of this repository (commit `2e2f9c1` and earlier) and in the upstream repository.

## License

MIT, see [LICENSE](LICENSE). Original author: MugishoMp.
