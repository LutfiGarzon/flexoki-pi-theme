# flexoki-pi-theme

[Flexoki](https://stephango.com/flexoki) color scheme themes for [pi](https://github.com/badlogic/pi-mono).

## Install

```bash
pi install npm:flexoki-pi-theme
# or from git:
pi install git:github.com/LutfiGarzon/flexoki-pi-theme
```

## Usage

Select via `/settings` in pi, or in `settings.json`:

```json
{ "theme": "flexoki-dark" }
```

Two variants are included:

| Theme | Background | Best for |
|-------|-----------|----------|
| `flexoki-dark` | `#100F0F` (black) | Dark terminals |
| `flexoki-light` | `#FFFCF0` (paper) | Light terminals |

## Color Palette

Flexoki is an inky color scheme with high contrast and warm tones. The palette is shared by both variants with adjusted luminance.

### Base Colors

| Token | Dark | Light | Role |
|-------|------|-------|------|
| `black` / `paper` | `#100F0F` | `#FFFCF0` | Background |
| `bg2` | `#282726` | `#F2F0E5` | Secondary background |
| `ui` | `#343331` | `#E6E4D9` | UI elements |
| `uiHover` | `#403E3C` | `#DAD8CE` | Hover state |
| `uiActive` | `#575653` | `#CECDC3` | Active state |

### Text

| Token | Dark | Light | Role |
|-------|------|-------|------|
| `tx` | `#CECDC3` | `#878580` | Primary text |
| `txMuted` | `#878580` | `#9F9D96` | Muted text |
| `txFaint` | `#575653` | `#CECDC3` | Dim text |

### Accents

| Token | Dark | Light | Role |
|-------|------|-------|------|
| `re` | `#D14D41` | `#AF3029` | Red (errors, removed) |
| `or` | `#DA702C` | `#BC5215` | Orange |
| `ye` | `#D0A215` | `#AD8301` | Yellow (warnings, headings) |
| `gr` | `#879A39` | `#66800B` | Green (success, added) |
| `cy` | `#3AA99F` | `#24837B` | Cyan (accent) |
| `bl` | `#4385BE` | `#205EA6` | Blue (links, keywords) |
| `pu` | `#8B7EC8` | `#5E409D` | Purple (custom labels) |
| `ma` | `#CE5D97` | `#A02F6F` | Magenta |

## Theme Tokens

Each theme defines all 51 required pi color tokens across these categories:

- **Core UI** (11): accent, borders, text, states
- **Backgrounds & Content** (11): message bubbles, tool status boxes
- **Markdown** (10): headings, links, code, quotes, lists
- **Tool Diffs** (3): added, removed, context lines
- **Syntax Highlighting** (9): comment, keyword, function, variable, string, number, type, operator, punctuation
- **Thinking Levels** (6): border colors for thinking modes
- **Bash Mode** (1): editor border for `!` prefix

For the full token reference, see the [pi themes documentation](https://github.com/badlogic/pi-mono/blob/main/packages/coding-agent/docs/themes.md#color-tokens).

## Customizing

1. Copy the theme you want to modify:
   ```bash
   cp themes/flexoki-dark.json ~/.pi/agent/themes/flexoki-dark-custom.json
   ```
2. Change `"name"` to `"flexoki-dark-custom"` (must be unique).
3. Edit colors — pi hot-reloads the active theme file on save.
4. Select via `/settings`.

## Contributing

- Report issues or suggest improvements on the [issue tracker](https://github.com/LutfiGarzon/flexoki-pi-theme/issues).
- Pull requests welcome for color refinements, new variants, or palette additions.

## License

MIT
