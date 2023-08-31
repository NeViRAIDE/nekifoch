<h1 align="center">Nekifoch</h1>
<h3 align="center">Neovim Kitty Font Changer</h3>
<hr>

<p align="center">
  <strong>Neovim plugin for managing Kitty terminal font settings.</strong>
</p>

<p align="center">
  <a href="#installation">Installation</a> •
  <a href="#usage">Usage</a> •
  <a href="#configuration">Configuration</a> •
  <a href="#functions-and-utilities">Functions and Utilities</a> •
  <a href="#credits">Credits</a> •
  <a href="#license">License</a> •
  <a href="#donations">Donations</a>
</p>

---

## Installation

Install Nekifoch using your favorite plugin manager. For example, with [lazy.nvim](https://github.com/folke/lazy.nvim):

```lua
{
    'RAprogramm/nekifoch',
    cmd = 'Nekifoch',
    opts = {}
}
```

## Usage

Nekifoch provides the `:Nekifoch` command with the following syntax:

```vim
:Nekifoch [action] [font_family]
```

- `[action]` can be one of: `check`, `write`, `list`.
- `[font_family]`: New font family for the `write` action.

Examples:

- Check the current font family:

```vim
:Nekifoch check
```

- Replace the font family with "DejaVu Sans Mono":

```vim
:Nekifoch write DejaVu Sans Mono
```

- List available fonts compatible with Kitty:

```vim
:Nekifoch list
```

## Configuration

Configure Nekifoch using the FontReplaceConfig dictionary:

Nekifoch can be configured by adding a Lua configuration to your Neovim configuration file (init.lua).

Here's an example configuration using Lua:

```lua
require('nekifoch').setup({
  kitty_conf_path = vim.fn.expand('~/.config/kitty/kitty.conf')
})
```

or

```lua
{
    'RAprogramm/nekifoch',
    opts = {
        kitty_conf_path = vim.fn.expand('~/.config/kitty/kitty.conf')
    }
}
```

Replace '~/.config/kitty/kitty.conf' with the actual path to your Kitty terminal configuration.

## Functions and Utilities

Nekifoch provides these utility functions:

- `get()`: Get the current font family from the Kitty configuration.
- `listInstalledFonts()`: List all installed fonts.
- `compareFontsWithKittyListFonts()`: Compare installed fonts with Kitty-compatible fonts.
- `replace_font_family(...)`: Replace the font family in the Kitty configuration.

## Credits

Developed by RAprogramm. Contributions are welcome.

## License

Distributed under the ... (not chosen yet).

For in-depth details and usage instructions, refer to the documentation.

<hr>

Enhance your Kitty terminal experience with Nekifoch

## Donations

If you find this plugin helpful and would like to support its development, you can buy me a coffee through the following platforms:

[![ko-fi](https://www.ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/rozanov)

[![buymeacoffee](https://img.buymeacoffee.com/button-api/?username=YOUR_BMC_USERNAME&button_colour=FFDD00&font_colour=000000&font_family=Cookie&outline_colour=000000)](https://www.buymeacoffee.com/raprogramm)

Your support is greatly appreciated!
