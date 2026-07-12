[Русский](README.ru.md) · [中文](README.zh.md) · [English](README.md)

# Matugen Obsidian Material 3

Une commande pour qu'Obsidian s'accorde à votre fond d'écran — un template Material You pour matugen.

## Fonctionnement

Exécutez `matugen image <fond>`, et Obsidian adopte la palette Material You de votre fond d'écran :

- Mode sombre / clair
- 139+ règles CSS (boutons, interrupteurs, navigation, menus, champs de saisie, recherche, curseurs, interface mobile, etc.)
- 98 tokens de couleur Material Design 3

## Installation

### 1. Ajoutez le template

```bash
cp templates/obsidian-minimal-matugen-colors.css ~/.config/matugen/templates/
```

### 2. Configurez matugen

Modifiez `~/.config/matugen/config.toml` :

```toml
[templates.Obsidian]
input_path = '~/.config/matugen/templates/obsidian-minimal-matugen-colors.css'
output_path = '/path/to/your/vault/.obsidian/snippets/obsidian-material3.css'
```

Voir `config/matugen-config-example.toml`.

### 3. Générez les couleurs

```bash
matugen image /path/to/wallpaper.jpg
```

### 4. Activez dans Obsidian

Paramètres → Apparence → Fragments CSS → activez `obsidian-material3.css`

> Si vous avez plusieurs coffres, copiez le template dans `.obsidian/snippets/` de chacun et ajoutez une entrée `[templates.Obsidian-XXX]` dédiée.

## Conseils de palette

Si le contraste est insuffisant (fréquent sur les fonds clairs), ajustez la configuration globale de matugen :

```toml
[config]
type = "SchemeVibrant"
contrast = 1.0
```

| Type | Effet |
|---|---|
| `SchemeTonalSpot` | Doux (par défaut) |
| `SchemeVibrant` | Vibrant |
| `SchemeExpressive` | Expressif |
| `SchemeFruitSalad` | Coloré et ludique |

## Remerciements

- [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3) par HarmfulBreeze — source des règles CSS
- [Matugen](https://github.com/InioX/matugen) par InioX — moteur de couleurs Material You
- [matugen-themes](https://github.com/InioX/matugen-themes) — référence de template

## Avertissement

Ce projet a été généré avec l'aide de l'IA (DeepSeek / opencode). Les règles CSS originales sont adaptées du [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3).
