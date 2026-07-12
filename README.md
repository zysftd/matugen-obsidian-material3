[Русский](README.ru.md) · [中文](README.zh.md) · [Français](README.fr.md)

# Matugen Obsidian Material 3

One command to make Obsidian match your wallpaper — a Material You matugen template.

## How it works

Run `matugen image <wallpaper>`, and Obsidian picks up the wallpaper's Material You color scheme with full:

- Dark / light dual mode
- 139+ CSS rules (buttons, switches, nav, menus, inputs, search, sliders, mobile, etc.)
- 98 Material Design 3 color tokens

## Installation

### 1. Add the template

```bash
cp templates/obsidian-minimal-matugen-colors.css ~/.config/matugen/templates/
```

### 2. Configure matugen

Edit `~/.config/matugen/config.toml` and add:

```toml
[templates.Obsidian]
input_path = '~/.config/matugen/templates/obsidian-minimal-matugen-colors.css'
output_path = '/path/to/your/vault/.obsidian/snippets/obsidian-material3.css'
```

See `config/matugen-config-example.toml` for reference.

### 3. Generate colors

```bash
matugen image /path/to/wallpaper.jpg
```

### 4. Enable in Obsidian

Settings → Appearance → CSS snippets → toggle `obsidian-material3.css`

> If you have multiple vaults, copy the template to each vault's `.obsidian/snippets/` and add a separate `[templates.Obsidian-XXX]` entry for each.

## Color scheme tips

If the generated colors lack contrast (common with light wallpapers), adjust the global matugen config:

```toml
[config]
type = "SchemeVibrant"
contrast = 1.0
```

| Type | Effect |
|---|---|
| `SchemeTonalSpot` | Soft (default) |
| `SchemeVibrant` | Vibrant |
| `SchemeExpressive` | Expressive |
| `SchemeFruitSalad` | Colorful & playful |

## Credits

- [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3) by HarmfulBreeze — source of the CSS rules
- [Matugen](https://github.com/InioX/matugen) by InioX — Material You color engine
- [matugen-themes](https://github.com/InioX/matugen-themes) — template reference

## Disclaimer

This project was generated with the assistance of AI (DeepSeek / opencode). The original CSS rules are adapted from the [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3).
