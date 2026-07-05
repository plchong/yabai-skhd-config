# yabai-skhd-config

A macOS tiling window manager configuration for developers using [yabai](https://github.com/koekeishiya/yabai) and [skhd](https://github.com/koekeishiya/skhd). All window operations use arrow keys for ergonomic control.

## Requirements

- macOS 14+
- [yabai](https://github.com/koekeishiya/yabai) (`brew install koekeishiya/formulae/yabai`)
- [skhd](https://github.com/koekeishiya/skhd) (`brew install koekeishiya/formulae/skhd`)

## Quick Start

```bash
git clone git@github.com:plchong/yabai-skhd-config.git ~/yabai-skhd-config
ln -sf ~/yabai-skhd-config/yabai/.yabairc ~/.yabairc
ln -sf ~/yabai-skhd-config/skhd/.skhdrc ~/.skhdrc
yabai --start-service
skhd --start-service
```

## Controls

| Category | Keys | Action |
|----------|------|--------|
| **Focus** | `Cmd+arrows` | Move focus between windows |
| **Swap** | `Shift+Cmd+arrows` | Swap focused window in direction |
| **Warp** | `Ctrl+Shift+Cmd+arrows` | Reinsert window in BSP tree (not swap) |
| **Resize** | `Ctrl+Cmd+arrows` | Resize active window |
| **Recent** | `Alt+Tab` | Focus previous window |
| **Spaces** | `Alt+1..9` | Switch to space N |
| **Move to Space** | `Shift+Alt+1..9` | Move window to space N |
| **Create/Delete Space** | `Ctrl+Alt+N/W` | Create or destroy space |
| **Float** | `Alt+D` | Toggle float on focused window |
| **Fullscreen** | `Alt+F` | Toggle fullscreen |
| **Layout** | `Alt+B` / `Alt+S` | BSP or Stack layout |
| **Rotate** | `Alt+R` | Rotate layout 90° |
| **Balance** | `Shift+Alt+R` | Even out window sizes |

## Display Hotplug

When disconnecting or reconnecting an external display, yabai automatically rebalances spaces and restarts skhd to restore IPC connectivity.

## macOS Permissions

1. Enable Accessibility permission for yabai and skhd (System Settings → Privacy & Security → Accessibility)
2. Enable "Displays have separate Spaces" (System Settings → Desktop & Dock → Mission Control)

## License

MIT
