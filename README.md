# Editor Width Slider (unlimited)

> ⚠️ **Written entirely by Claude or another AI model** (Claude is Anthropic's AI assistant). No human has reviewed the code line by line. Use at your own risk.
> ⚠️ **Написано полностью Клодом или другой ИИ-моделью** (Клод — ИИ-ассистент Anthropic). Построчной проверки кода человеком не было. Используйте на свой риск.

<details>
<summary><b>🇬🇧 English</b></summary>

Fork of [MugishoMp/obsidian-editor-width-slider](https://github.com/MugishoMp/obsidian-editor-width-slider) (MIT). This repository holds only the built plugin: `main.js` and `manifest.json`.

## What changed

The slider in the status bar now runs from 700px (slider at 0) to the full window width (slider at 100). In the original the range ended at 1700px, so on wide screens the margins never went away.

The formula, in the two CSS variables the plugin sets:

```
calc(700px + <slider> * (100vw - 700px) / 100)
```

The plugin id is `yule-width-slider-unlim` (the original is `editor-width-slider`). Both plugins use the same slider and style element, so keep only one of them enabled. Settings are stored per plugin folder: to keep the saved slider position, copy `data.json` from the original plugin folder.

## Requirements

Obsidian applies `--line-width` and `--file-line-width` only when "Readable line length" is on (Settings → Editor). Keep it enabled.

## Installation

1. Download `main.js` and `manifest.json` from this repository.
2. Put them in `<vault>/.obsidian/plugins/yule-width-slider-unlim/`.
3. Disable the original Editor Width Slider if it is installed, restart Obsidian and enable this plugin in Settings → Community plugins.

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

</details>

<details>
<summary><b>🇷🇺 Русский</b></summary>

Форк [MugishoMp/obsidian-editor-width-slider](https://github.com/MugishoMp/obsidian-editor-width-slider) (MIT). Этот репозиторий содержит только собранный плагин: `main.js` и `manifest.json`.

## Что изменилось

Ползунок в строке состояния теперь идёт от 700px (ползунок в 0) до полной ширины окна (ползунок в 100). В оригинале диапазон заканчивался на 1700px, поэтому на широких экранах поля не исчезали.

Формула в двух CSS-переменных, которые задаёт плагин:

```
calc(700px + <ползунок> * (100vw - 700px) / 100)
```

Идентификатор плагина `yule-width-slider-unlim` (у оригинала `editor-width-slider`). Оба плагина используют один и тот же ползунок и один и тот же элемент стиля, поэтому включайте только один из них. Настройки хранятся в папке каждого плагина отдельно: чтобы сохранить положение ползунка, скопируйте `data.json` из папки оригинального плагина.

## Требования

Obsidian применяет `--line-width` и `--file-line-width` только при включённой опции «Readable line length» (Настройки → Редактор). Оставьте её включённой.

## Установка

1. Скачайте `main.js` и `manifest.json` из этого репозитория.
2. Положите их в `<хранилище>/.obsidian/plugins/yule-width-slider-unlim/`.
3. Отключите оригинальный Editor Width Slider, если он установлен, перезапустите Obsidian и включите этот плагин в Настройки → Сторонние плагины.

## Использование

Перетаскивайте ползунок в строке состояния. Щелчок по числу рядом с ним сбрасывает ширину.

У отдельной заметки может быть своя ширина: добавьте `editor-width` (от 0 до 100) в YAML-шапку (frontmatter) заметки.

```yaml
---
editor-width: 75
---
```

## Исходный код

Исходный код находится в истории этого репозитория (коммит `2e2f9c1` и более ранние) и в исходном репозитории.

## Лицензия

MIT, см. [LICENSE](LICENSE). Автор оригинала: MugishoMp.

</details>
