# Workspace Hover Cards

Omarchy bar widget: workspace number indicators with a rich hover card that shows
exactly what is running on each workspace.

## Features

- **Live hover card** — hovering a workspace chip shows its name, window count,
  and a per-window list of app icon + window title, instead of the plain
  "Workspace N" tooltip bubble.
- **Accurate app icons** — resolves icons through desktop entries, handling both
  Wayland `appId` and XWayland `class` (e.g. `Google-chrome` → Google Chrome →
  the right icon).
- **Webapp icons** — browser windows are matched by the site name carried in the
  window title (e.g. "Home / X" gets the X icon), so webapps don't all show a
  generic browser icon.
- **Steam games** — `steam_app_<id>` surfaces are resolved to the actual game
  name and icon via the window title.

## Install

```bash
omarchy plugin add https://github.com/L0nE-F0x/lonefox.workspaces.git --enable
```

Then place it on the bar. Replace the built-in workspaces widget if you use one:

```bash
omarchy bar put lonefox.workspaces --section left
# or, if it is already on the bar:
omarchy bar move lonefox.workspaces --section left
```

## Remove

```bash
omarchy plugin remove lonefox.workspaces --yes
```

## License

MIT — see [LICENSE](LICENSE).
