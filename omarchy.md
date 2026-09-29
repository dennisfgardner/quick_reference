# Omarchy Quick Reference

## Modifier Logic

`SUPER` is the leader key for almost everything. What's added to it tells you the *kind* of action:

| Modifier added to SUPER | Reads as |
|---|---|
| (none) | do the core thing to the focused window |
| `SHIFT` | move it / open it / reverse direction |
| `CTRL` | system control, not the window |
| `ALT` | alternate / secondary / finer variant |

Triple combos stack meanings (e.g. `SHIFT+ALT` = move it, the alternate way). Not airtight — a few bindings just dodge letter collisions — but that's the intent. Note: Linux/Hyprland calls it `ALT`, not "Opt" (macOS Option).

## Tiling Window Management

| Function | Shortcut |
|----------|----------|
| Close Window | `SUPER + W` |
| Send Window to *Nth* Workspace | `SUPER + SHIFT + <N>` |
| Go to *Nth* Workspace | `SUPER + <N>` |
| Move Focus | `SUPER + ARROW` |
| Swap Windows | `SUPER + SHIFT + ARROW` |
| Toggle Horz/Vert Split | `SUPER + J` |
| Toggle Float or Tiled | `SUPER + T` |

## Basic

| Function | Shortcut |
|----------|----------|
| Omarchy Menu | `SUPER + SPACE` |
| Keyboard Bindings | `SUPER + K` |
| WiFi settings | `SUPER + CRTL + W` |
| Bluetooth | `SUPER + CTRL + B` | 
| Battery | `SUPER + ALT + CTRL + B` |
| Web Browser | `SUPER + SHIFT + RETURN` or `SUPER + SHIFT + B` |

## Open Apps

| Function | Shortcut |
|----------|----------|
| App Menu | `SUPER + ALT + SPACE` |
| Terminal | `SUPER + RETURN` |
| Tmux | `SUPER + ALT + RETURN` |
| Herdr | `SUPER + CTRL + RETURN`|
| X (aka Twitter) | `SUPER + SHIFT + X` |
| Calendar | `SUPER + SHIFT + C` |

## System Control

| Function | Shortcut |
|----------|----------|
| Audio |     `SUPER + CTRL + A` |
| Bluetooth | `SUPER + CTRL + B` | 
| Battery |   `SUPER + CTRL + ALT + B` |
| WiFi |      `SUPER + CRTL + W` |

## Updating

- `omarchy update` — system/GUI apps & packages (VS Code, pacman/AUR, Omarchy itself)
- `mise upgrade` — all mise-managed CLI/dev tools at once (node, gh, claude, codex, etc.)
- `mise upgrade <pkg>` — just one mise-managed tool, e.g. mise upgrade node