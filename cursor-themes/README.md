# Cursor / VS Code themes

Local color themes. They are folders, not marketplace installs.

| Folder | Theme name in the picker | What it is |
|---|---|---|
| `defron.my-dark-plus-black-1.0.0` | **My Dark+ Black** | Dark+ Tweaked, pitch-black walls, Dark+ status bar (darker), AdaLabs splits |
| `defron.my-dark-2026-1.0.0` | **My Dark 2026** | Dark 2026 Green syntax and green accents, same black walls, same status bar and cursor as My Dark+ Black |
| `defron.my-one-dark-2026-1.0.0` | **My One Dark 2026** | One Dark 2026 Pro syntax, same black walls, same status bar and cursor as My Dark+ Black |
| `defron.my-dark-cursor-theme-1.0.0` | **My Dark Cursor Theme** | Cursor Dark syntax and accents, pitch-black walls, caret `#9fcb80` |
| `defron.my-atom-one-light-1.0.0` | **My Atom One Light** | Atom One Light syntax, Dimmed Light 2026 walls, Light+ activity bar (icon rail) and status bar. Tab-bar icon buttons use `#a1a1a1` |
| `defron.my-light-2026-dimmed-1.0.0` | **My Light 2026 Dimmed** | Dimmed Light 2026 syntax, same chrome as My Atom One Light |
| `defron.my-light-plus-1.0.0` | **My Light+** | Light+ syntax, same chrome as My Atom One Light |
| `defron.my-light-2026-1.0.0` | **My Light 2026** | Dimmed Light 2026 syntax, Light+ chrome |

A theme is a slot in the Color Theme list. Cursor and VS Code only see it if the folder sits in their **extensions** directory.

## Install (this machine or another)

Copy **each theme folder** into the extensions directory. Keep the folder name as-is (`publisher.name-version`).

**Cursor**

```bash
# Windows (Git Bash)
cp -R defron.my-dark-plus-black-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-dark-2026-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-one-dark-2026-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-dark-cursor-theme-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-atom-one-light-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-light-2026-dimmed-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-light-plus-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-light-2026-1.0.0 "$HOME/.cursor/extensions/"

# macOS / Linux
cp -R defron.my-dark-plus-black-1.0.0 ~/.cursor/extensions/
cp -R defron.my-dark-2026-1.0.0 ~/.cursor/extensions/
cp -R defron.my-one-dark-2026-1.0.0 ~/.cursor/extensions/
cp -R defron.my-dark-cursor-theme-1.0.0 ~/.cursor/extensions/
cp -R defron.my-atom-one-light-1.0.0 ~/.cursor/extensions/
cp -R defron.my-light-2026-dimmed-1.0.0 ~/.cursor/extensions/
cp -R defron.my-light-plus-1.0.0 ~/.cursor/extensions/
cp -R defron.my-light-2026-1.0.0 ~/.cursor/extensions/
```

**VS Code**

```bash
# Windows (Git Bash)
cp -R defron.my-dark-plus-black-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-dark-2026-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-one-dark-2026-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-dark-cursor-theme-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-atom-one-light-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-light-2026-dimmed-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-light-plus-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-light-2026-1.0.0 "$HOME/.vscode/extensions/"

# macOS / Linux
cp -R defron.my-dark-plus-black-1.0.0 ~/.vscode/extensions/
cp -R defron.my-dark-2026-1.0.0 ~/.vscode/extensions/
cp -R defron.my-one-dark-2026-1.0.0 ~/.vscode/extensions/
cp -R defron.my-dark-cursor-theme-1.0.0 ~/.vscode/extensions/
cp -R defron.my-atom-one-light-1.0.0 ~/.vscode/extensions/
cp -R defron.my-light-2026-dimmed-1.0.0 ~/.vscode/extensions/
cp -R defron.my-light-plus-1.0.0 ~/.vscode/extensions/
cp -R defron.my-light-2026-1.0.0 ~/.vscode/extensions/
```

Windows Explorer paths if you prefer not to use a shell:

| App | Folder |
|---|---|
| Cursor | `%USERPROFILE%\.cursor\extensions` |
| VS Code | `%USERPROFILE%\.vscode\extensions` |

If a folder with the same name is already there, replace it. Do not nest one copy inside the other (the theme file must sit at `.../themes/*.json` one level under the extension folder, not two).

Then:

1. Reload the window: **Ctrl+Shift+P** (macOS **Cmd+Shift+P**) → **Developer: Reload Window**
2. **Ctrl+K Ctrl+T** (macOS **Cmd+K Cmd+T**) → pick **My Dark+ Black**, **My Dark 2026**, **My One Dark 2026**, **My Dark Cursor Theme**, **My Atom One Light**, **My Light 2026 Dimmed**, **My Light+**, or **My Light 2026**

To make it the dark theme when the OS is in dark mode, set **Preferences: Color Theme** preferred dark, or in `settings.json`:

```json
"workbench.preferredDarkColorTheme": "My Dark 2026"
```

Use `"My Dark+ Black"` if that is the one you want.

For the light theme when the OS is in light mode:

```json
"workbench.preferredLightColorTheme": "My Atom One Light"
```

## After a git pull on a new machine

From this `cursor-themes` directory, run the same `cp -R` commands as above, then reload.

**My Dark 2026** includes a local copy of Dark 2026 Green’s syntax file (`themes/dark-2026-green-base.json`). **My One Dark 2026** includes a local copy of One Dark 2026 Pro (`themes/one-dark-2026-pro-base.json`). **My Dark Cursor Theme** includes a local copy of Cursor Dark (`themes/cursor-dark-base.json`). **My Atom One Light** includes a local copy of Atom One Light (`themes/one-light-base.json`). **My Light 2026 Dimmed** and **My Light 2026** include Dimmed Light 2026 syntax. **My Light+** includes Light+ syntax. You do not need those marketplace extensions installed, as long as those base files are present.

## Layout

```
cursor-themes/
  README.md
  defron.my-dark-plus-black-1.0.0/
    package.json
    themes/My Dark+ Black-color-theme.json
  defron.my-dark-2026-1.0.0/
    package.json
    themes/My Dark 2026-color-theme.json
    themes/dark-2026-green-base.json
  defron.my-one-dark-2026-1.0.0/
    package.json
    themes/My One Dark 2026-color-theme.json
    themes/one-dark-2026-pro-base.json
  defron.my-dark-cursor-theme-1.0.0/
    package.json
    themes/My Dark Cursor Theme-color-theme.json
    themes/cursor-dark-base.json
  defron.my-atom-one-light-1.0.0/
    package.json
    themes/My Atom One Light-color-theme.json
    themes/one-light-base.json
  defron.my-light-2026-dimmed-1.0.0/
    package.json
    themes/My Light 2026 Dimmed-color-theme.json
    themes/dimmed-light-2026-syntax.json
    themes/my-atom-one-light-chrome.json
  defron.my-light-plus-1.0.0/
    package.json
    themes/My Light+-color-theme.json
    themes/light-plus-syntax.json
    themes/my-atom-one-light-chrome.json
  defron.my-light-2026-1.0.0/
    package.json
    themes/My Light 2026-color-theme.json
    themes/dimmed-light-2026-syntax.json
```

`package.json` is the label the picker shows. The JSON under `themes/` is the paint (chrome colors and token colors).
