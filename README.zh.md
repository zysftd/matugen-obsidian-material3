[Русский](README.ru.md) · [Français](README.fr.md) · [English](README.md)

# Matugen Obsidian Material 3

一键让 Obsidian 跟随壁纸配色 — 基于 Material You 的 Matugen 模板。

## 效果

运行 `matugen image <壁纸>`，Obsidian 自动套用壁纸的 Material You 配色方案，包含完整的：

- 暗色/亮色双模式
- 139+ CSS 样式规则（按钮、开关、导航、菜单、输入框、搜索、滑块、移动端界面等）
- 98 个 Material Design 3 颜色令牌

## 安装

### 1. 添加模板

```bash
cp templates/obsidian-minimal-matugen-colors.css ~/.config/matugen/templates/
```

### 2. 配置 Matugen

编辑 `~/.config/matugen/config.toml`：

```toml
[templates.Obsidian]
input_path = '~/.config/matugen/templates/obsidian-minimal-matugen-colors.css'
output_path = '/path/to/your/vault/.obsidian/snippets/obsidian-material3.css'
```

参考 `config/matugen-config-example.toml`。

### 3. 生成配色

```bash
matugen image /path/to/wallpaper.jpg
```

### 4. 在 Obsidian 中启用

设置 → 外观 → CSS 代码片段 → 启用 `obsidian-material3.css`

> 如果有多个知识库，每个库的 `.obsidian/snippets/` 都要添加并配置单独的 `[templates.Obsidian-XXX]` 条目。

## 调色建议

如果生成的配色对比度不够（常见于浅色壁纸），可以在 Matugen 全局配置中调整：

```toml
[config]
type = "SchemeVibrant"
contrast = 1.0
```

| 类型 | 效果 |
|---|---|
| `SchemeTonalSpot` | 柔和（默认） |
| `SchemeVibrant` | 鲜艳 |
| `SchemeExpressive` | 富有表现力 |
| `SchemeFruitSalad` | 多彩活泼 |

## 致谢

- [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3) by HarmfulBreeze — CSS 样式规则来源
- [Matugen](https://github.com/InioX/matugen) by InioX — Material You 颜色生成引擎
- [matugen-themes](https://github.com/InioX/matugen-themes) — 模板参考

## 声明

本项目由 AI（DeepSeek / opencode）辅助生成，原始 CSS 规则基于 [Material 3 Obsidian Theme](https://github.com/HarmfulBreeze/obsidian-material-3) 转换适配。
