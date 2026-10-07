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

**Use `SUPER + K` to look up shortcuts.**

## Window Management

| Function | Shortcut |
|----------|----------|
| Close Window | `SUPER + W` |
| Send Window to *Nth* Workspace | `SUPER + SHIFT + <N>` |
| Go to *Nth* Workspace | `SUPER + <N>` |
| Move Focus | `SUPER + ARROW` |
| Swap Windows | `SUPER + SHIFT + ARROW` |
| Toggle Horz/Vert Split | `SUPER + J` |
| Toggle Float or Tiled | `SUPER + T` |
| Toggle Scratch Pad | `SUPER + S` |
| Toggle Dwindle/Scrolling | `SUPER + L` |
| Move Window | `SUPER + Right MOUSE BUTTONs` |
| Resize Window | `SUPER + LEFT MOUSE BUTTON` |
| Google Gap | `SUPER + SHIFT + BACKSPACE` |

## Open Apps

| Function | Shortcut |
|----------|----------|
| Omarchy Menu | `SUPER + SPACE` |
| App Menu | `SUPER + ALT + SPACE` |
| Terminal | `SUPER + RETURN` |
| Web Browser | `SUPER + SHIFT + RETURN` or `SUPER + SHIFT + B` |
| Calendar | `SUPER + SHIFT + C` |
| Agent | `SUPER + CTRL + SHIFT + A` |
| Weather | `SUPER + CTRL + ALT + W` |
| Tmux | `SUPER + ALT + RETURN` |
| Herdr | `SUPER + CTRL + RETURN`|
| X (aka Twitter) | `SUPER + SHIFT + X` |

## System Control

| Function | Shortcut |
|----------|----------|
| Audio |     `SUPER + CTRL + A` |
| Bluetooth | `SUPER + CTRL + B` | 
| Battery |   `SUPER + CTRL + ALT + B` |
| WiFi |      `SUPER + CTRL + W` |
| Lock Computer | `SUPER + L` |
| Computer Menu | `SUPER + ESC`|

## Updating

- `omarchy update` — system/GUI apps & packages (VS Code, pacman/AUR, Omarchy itself)
- `mise upgrade` — all mise-managed CLI/dev tools at once (node, gh, claude, codex, etc.)
- `mise upgrade <pkg>` — just one mise-managed tool, e.g. mise upgrade node

## Creating/Linking Web App

1. First open the Omarchy Menu: `SUPER + SPACE`
2. Use arrow keys to select and move into `Install` menu
3. Select Web App
4. Name it and then provide link
