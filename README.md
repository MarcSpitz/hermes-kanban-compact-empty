# Hermes Kanban Compact Empty

A standalone Hermes Dashboard theme that turns Kanban columns with no tasks into narrow vertical rails. It keeps active columns card-friendly and preserves the **+** action on folded columns.

![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

## What it changes

- Active Kanban columns keep a minimum width of **280px** and share available horizontal space.
- Columns that display Hermes’ built-in empty state collapse to a **52px** rail.
- Folded columns show a vertical status label and the **+** create-task button.
- The empty helper message, task count, and body are hidden on folded columns.

The theme mirrors Hermes’ built-in **Hermes Teal (Large)** appearance, so the Kanban layout is the only intentional visual change.

## Install

```bash
git clone https://github.com/MarcSpitz/hermes-kanban-compact-empty.git
cd hermes-kanban-compact-empty

THEMES_DIR="${HERMES_HOME:-$HOME/.hermes}/dashboard-themes"
mkdir -p "$THEMES_DIR"
cp kanban-compact-empty.yaml "$THEMES_DIR/"

hermes config set dashboard.theme kanban-compact-empty
```

Refresh the Hermes Dashboard after installation. The theme is also selectable from the Dashboard theme picker as **Hermes Teal (Large) — Compact Empty Kanban**.

### Profile-scoped Hermes

If Hermes runs under a named profile, set `HERMES_HOME` to that profile before installing. For example:

```bash
export HERMES_HOME="$HOME/.hermes/profiles/grand-schtroumpf"
```

Then run the install commands above.

## Compatibility

This is a CSS-only customization for the bundled Hermes Dashboard Kanban plugin. It uses the plugin’s current CSS class names and the modern CSS `:has()` selector. After upgrading Hermes, quickly confirm that folded columns still render as expected; a future Kanban markup change may require a selector update.

## License

[MIT](LICENSE) © 2026 Kevin Jadin
