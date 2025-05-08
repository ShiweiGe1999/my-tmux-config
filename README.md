# My Tmux Configuration

This repository contains my personal tmux configuration based on [Oh My Tmux!](https://github.com/gpakosz/.tmux) by Gregory Pakosz. It features a beautiful Catppuccin Mocha theme, sensible defaults, and easy customization options.

## Features

- Beautiful Catppuccin Mocha color scheme
- Intuitive key bindings
- Status bar with useful information
- Mouse mode support
- Easy customization through `.tmux.conf.local`
- Plugin support via TPM (Tmux Plugin Manager)

## Installation

### Prerequisites

- Git
- Tmux (version 2.6 or newer recommended)

### Quick Install

1. Clone this repository to your home directory:

```bash
git clone https://github.com/ShiweiGe1999/my-tmux-config.git ~/.tmux-config
```

2. Create symbolic links to the configuration files:

```bash
ln -s -f ~/.tmux-config/.tmux.conf ~/.tmux.conf
ln -s -f ~/.tmux-config/.tmux.conf.local ~/.tmux.conf.local
```

3. Start or restart tmux:

```bash
# If tmux is already running
tmux source-file ~/.tmux.conf

# Or start a new tmux session
tmux
```

### Manual Installation

If you prefer to copy the files instead of using symbolic links:

1. Clone this repository:

```bash
git clone https://github.com/ShiweiGe1999/my-tmux-config.git ~/my-tmux-config
```

2. Copy the configuration files to your home directory:

```bash
cp ~/my-tmux-config/.tmux.conf ~/.tmux.conf
cp ~/my-tmux-config/.tmux.conf.local ~/.tmux.conf.local
```

3. Start or restart tmux:

```bash
# If tmux is already running
tmux source-file ~/.tmux.conf

# Or start a new tmux session
tmux
```

## Customization

You can customize your tmux configuration by editing the `.tmux.conf.local` file. This file contains various options that you can modify without changing the main configuration file.

Some common customizations:

- Change the theme colors
- Modify key bindings
- Enable/disable features
- Add plugins

Example:

```bash
# Edit your local configuration
nano ~/.tmux.conf.local

# After making changes, reload tmux configuration
tmux source-file ~/.tmux.conf
```

## Key Bindings

The prefix key is set to `Ctrl+a` (you can also use the default `Ctrl+b`).

Some useful key bindings:

- `<prefix> c`: Create a new window
- `<prefix> -`: Split window horizontally
- `<prefix> _`: Split window vertically
- `<prefix> h/j/k/l`: Navigate between panes
- `<prefix> H/J/K/L`: Resize panes
- `<prefix> Tab`: Switch to the last active window
- `<prefix> C-h/C-l`: Navigate between windows
- `<prefix> m`: Toggle mouse mode
- `<prefix> r`: Reload tmux configuration
- `<prefix> e`: Edit tmux configuration

## Plugins

This configuration supports [TPM (Tmux Plugin Manager)](https://github.com/tmux-plugins/tpm) for easy plugin management.

To add plugins, uncomment and modify the plugin section in your `.tmux.conf.local` file:

```bash
# Add these lines to your .tmux.conf.local
set -g @plugin 'tmux-plugins/tmux-resurrect'
set -g @plugin 'tmux-plugins/tmux-continuum'
```

After adding plugins:
- Press `<prefix> + I` to install plugins
- Press `<prefix> + u` to update plugins
- Press `<prefix> + Alt + u` to uninstall plugins

## Troubleshooting

If you encounter any issues:

1. Make sure you have tmux version 2.6 or newer:
   ```bash
   tmux -V
   ```

2. Check for error messages when starting tmux:
   ```bash
   tmux -v
   ```

3. Verify that your terminal supports 256 colors:
   ```bash
   echo $TERM
   ```
   It should output something like `screen-256color` or `xterm-256color`.

4. If plugins aren't working, make sure TPM is properly installed:
   ```bash
   ls -la ~/.tmux/plugins/tpm
   ```

## Credits

- [Oh My Tmux!](https://github.com/gpakosz/.tmux) by Gregory Pakosz
- [Catppuccin](https://github.com/catppuccin/tmux) for the color scheme inspiration

## License

This configuration is dual-licensed under the WTFPL v2 license and the MIT license, without any warranty, following the original Oh My Tmux! licensing.
