[中文](README.zh.md) · [Français](README.fr.md) · [English](README.md)

# Matugen Obsidian Material 3

Одна команда, чтобы Obsidian соответствовал вашим обоям — шаблон Material You для matugen.

## Как это работает

Запустите `matugen image <обои>`, и Obsidian применит цветовую схему Material You из ваших обоев:

- Тёмный / светлый режимы
- 139+ CSS-правил (кнопки, переключатели, навигация, меню, поля ввода, поиск, ползунки, мобильный интерфейс и т.д.)
- 98 цветовых токенов Material Design 3

## Установка

### 1. Добавьте шаблон

```bash
cp templates/obsidian-minimal-matugen-colors.css ~/.config/matugen/templates/
```

### 2. Настройте matugen

Отредактируйте `~/.config/matugen/config.toml`:

```toml
[templates.Obsidian]
input_path = '~/.config/matugen/templates/obsidian-minimal-matugen-colors.css'
output_path = '/path/to/your/vault/.obsidian/snippets/obsidian-material3.css'
```

См. `config/matugen-config-example.toml`.

### 3. Сгенерируйте цвета

```bash
matugen image /path/to/wallpaper.jpg
```

### 4. Включите в Obsidian

Настройки → Внешний вид → CSS-фрагменты → включите `obsidian-material3.css`

> Если у вас несколько хранилищ, скопируйте шаблон в `.obsidian/snippets/` каждого и добавьте отдельный `[templates.Obsidian-XXX]`.

## Советы по схеме цветов

Если контраст недостаточен (обычно на светлых обоях), настройте глобальный конфиг matugen:

```toml
[config]
type = "SchemeVibrant"
contrast = 1.0
```

| Тип | Эффект |
|---|---|
| `SchemeTonalSpot` | Мягкий (по умолчанию) |
| `SchemeVibrant` | Яркий |
| `SchemeExpressive` | Выразительный |
| `SchemeFruitSalad` | Красочный и игривый |

## Благодарности

- [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3) от HarmfulBreeze — исходный код CSS
- [Matugen](https://github.com/InioX/matugen) от InioX — движок цветов Material You
- [matugen-themes](https://github.com/InioX/matugen-themes) — пример для шаблона

## Отказ от ответственности

Этот проект создан с помощью ИИ (DeepSeek / opencode). Оригинальные CSS-правила адаптированы из [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3).
