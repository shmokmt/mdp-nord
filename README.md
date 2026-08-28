# mdp-nord

A [Nord](https://www.nordtheme.com/) theme for
[masawada/mdp](https://github.com/masawada/mdp) — an arctic, north-bluish
color scheme for a clean, dark, low-contrast Markdown preview.

## Preview

![Screenshot of mdp rendering examples/demo.md with the Nord theme](./screenshot.png)

*Rendered from [`examples/demo.md`](./examples/demo.md).*

The theme renders Markdown with:

- A dark **Polar Night** background (`#2e3440`) with **Snow Storm** body text (`#d8dee9`)
- **Frost** blues for headings, links, and blockquote accents
- **Aurora** accents for inline code (yellow), checked task-list checkboxes (green), and strikethrough text
- Styling for GFM tables, task lists, footnotes, `<kbd>`, blockquotes, code blocks, and horizontal rules
- A responsive layout (max width `780px`) that works well on both desktop and mobile

## Installation

`mdp` loads theme templates from a `themes/` directory inside its **config
directory**. The config directory is the directory containing your
`config.yaml`, resolved from (in priority order):

1. The `--config` flag you pass to `mdp`
2. `$UserConfigDir/mdp/config.yaml` (macOS: `~/Library/Application Support/mdp`)
3. `$HOME/.config/mdp/config.yaml` (Linux, or macOS via `$XDG_CONFIG_HOME`)

### 1. Download the theme

Copy `nord.html` into the `themes/` directory under your `mdp` config
directory, keeping the filename `nord.html` (the theme name mdp uses is the
filename without the `.html` extension).

**macOS**

```bash
mkdir -p ~/Library/Application\ Support/mdp/themes
curl -o ~/Library/Application\ Support/mdp/themes/nord.html \
  https://raw.githubusercontent.com/shmokmt/mdp-nord/main/nord.html
```

**Linux**

```bash
mkdir -p ~/.config/mdp/themes
curl -o ~/.config/mdp/themes/nord.html \
  https://raw.githubusercontent.com/shmokmt/mdp-nord/main/nord.html
```

Or clone this repository and copy the file locally:

```bash
git clone https://github.com/shmokmt/mdp-nord.git
mkdir -p ~/.config/mdp/themes        # or the macOS path above
cp mdp-nord/nord.html ~/.config/mdp/themes/nord.html
```

### 2. Enable the theme in your config

Edit (or create) your `config.yaml` in the same config directory and set
`theme` to `nord`:

```yaml
# ~/.config/mdp/config.yaml (or the macOS equivalent)
theme: nord
```

### 3. Run mdp

```bash
mdp README.md
```

Your resulting directory layout should look like this:

```
~/.config/mdp/
├── config.yaml
└── themes/
    └── nord.html
```

## Using it for a single file only

If you don't want to set Nord as your global default theme, point `--config`
at a dedicated config file that has `theme: nord` set, and use it only when
you want the Nord look:

```bash
mdp --config ~/.config/mdp/nord-config.yaml README.md
```

## Credits

- Color palette: [Nord](https://www.nordtheme.com/) by Sven Greb, licensed
  under [MIT](https://github.com/nordtheme/nord/blob/develop/LICENSE.md).
- Theme template for [mdp](https://github.com/masawada/mdp).

## License

MIT — see [LICENSE](./LICENSE).
