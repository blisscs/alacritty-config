# Alacritty Config

Personal Alacritty terminal configuration matching a Hyprland/ashell visual style.

**Theme:** Catppuccin Latte
**Font:** JetBrainsMono Nerd Font, 13pt
**Window:** Maximized, no decorations, 95% opacity

## Prerequisites

- [Alacritty](https://alacritty.org/)
- [JetBrainsMono Nerd Font](https://www.nerdfonts.com/font-downloads)

## Installation

1. Clone with submodules:
   ```sh
   git clone --recurse-submodules <repo-url> alacritty-config
   ```
   Or if already cloned:
   ```sh
   git submodule update --init --recursive
   ```

2. Symlink into Alacritty's config directory (run from this repo's root):
   ```sh
   mkdir -p ~/.config/alacritty
   ln -s "$PWD/alacritty.toml" ~/.config/alacritty/alacritty.toml
   ln -s "$PWD/alacritty-theme" ~/.config/alacritty/alacritty-theme
   ```

## Changing the Theme

Edit the `import` line in `alacritty.toml` to use any theme from the `alacritty-theme/themes/` directory:

```toml
[general]
import = [
    "~/.config/alacritty/alacritty-theme/themes/<theme-name>.toml"
]
```

See all available themes at [alacritty/alacritty-theme](https://github.com/alacritty/alacritty-theme).

## Keybindings

| Key           | Action                                       |
|---------------|----------------------------------------------|
| `Shift+Enter` | Send escape sequence (`\e\r`) for app compat |
