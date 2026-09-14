# Cursor / VS Code themes

Two local color themes. They are folders, not marketplace installs.

| Folder | Theme name in the picker | What it is |
|---|---|---|
| `defron.my-dark-plus-black-1.0.0` | **My Dark+ Black** | Dark+ Tweaked, pitch-black walls, Dark+ status bar (darker), AdaLabs splits |
| `defron.my-dark-2026-1.0.0` | **My Dark 2026** | Dark 2026 Green syntax and green accents, same black walls, same status bar and cursor as My Dark+ Black |

A theme is a slot in the Color Theme list. Cursor and VS Code only see it if the folder sits in their **extensions** directory.

## Install (this machine or another)

Copy **each theme folder** into the extensions directory. Keep the folder name as-is (`publisher.name-version`).

**Cursor**

```bash
# Windows (Git Bash)
cp -R defron.my-dark-plus-black-1.0.0 "$HOME/.cursor/extensions/"
cp -R defron.my-dark-2026-1.0.0 "$HOME/.cursor/extensions/"

# macOS / Linux
cp -R defron.my-dark-plus-black-1.0.0 ~/.cursor/extensions/
cp -R defron.my-dark-2026-1.0.0 ~/.cursor/extensions/
```

**VS Code**

```bash
# Windows (Git Bash)
cp -R defron.my-dark-plus-black-1.0.0 "$HOME/.vscode/extensions/"
cp -R defron.my-dark-2026-1.0.0 "$HOME/.vscode/extensions/"

# macOS / Linux
cp -R defron.my-dark-plus-black-1.0.0 ~/.vscode/extensions/
cp -R defron.my-dark-2026-1.0.0 ~/.vscode/extensions/
```

Windows Explorer paths if you prefer not to use a shell:

| App | Folder |
|---|---|
| Cursor | `%USERPROFILE%\.cursor\extensions` |
| VS Code | `%USERPROFILE%\.vscode\extensions` |

If a folder with the same name is already there, replace it. Do not nest one copy inside the other (the theme file must sit at `.../themes/*.json` one level under the extension folder, not two).

Then:

1. Reload the window: **Ctrl+Shift+P** (macOS **Cmd+Shift+P**) → **Developer: Reload Window**
2. **Ctrl+K Ctrl+T** (macOS **Cmd+K Cmd+T**) → pick **My Dark+ Black** or **My Dark 2026**

To make it the dark theme when the OS is in dark mode, set **Preferences: Color Theme** preferred dark, or in `settings.json`:

```json
"workbench.preferredDarkColorTheme": "My Dark 2026"
```

Use `"My Dark+ Black"` if that is the one you want.

## After a git pull on a new machine

From this `cursor-themes` directory, run the same `cp -R` commands as above, then reload.

**My Dark 2026** includes a local copy of Dark 2026 Green’s syntax file (`themes/dark-2026-green-base.json`). You do not need the marketplace Green extension installed for it to work, as long as that file is present.

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
```

`package.json` is the label the picker shows. The JSON under `themes/` is the paint (chrome colors and token colors).
