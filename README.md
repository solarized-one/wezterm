```lua
-- touch ~/.wezterm.lua

local wezterm = require("wezterm")
local config = wezterm.config_builder()

-- General
config.font = wezterm.font("Inconsolata")
config.font_size = 17
config.line_height = 1.2
config.default_cursor_style = "SteadyBar"

-- Theme 
config.colors = {
  foreground = "#f8f8f2",
  background = "#1e2127",
  cursor_bg = "#6c71c4",
  cursor_fg = "#6c71c4",
  cursor_border = "#6c71c4",

  ansi = {
    "#073642", -- black
    "#dc322f", -- red
    "#859900", -- green
    "#b58900", -- yellow
    "#268bd2", -- blue
    "#d33682", -- magenta
    "#2aa198", -- cyan
    "#eee8d5", -- white
  },
  brights = {
    "#002b36", -- bright black
    "#cb4b16", -- bright red (your accent)
    "#586e75", -- bright green
    "#657b83", -- bright yellow
    "#839496", -- bright blue
    "#6c71c4", -- bright magenta
    "#93a1a1", -- bright cyan
    "#fdf6e3", -- bright white
  },
}

-- Window
config.window_close_confirmation = "NeverPrompt"
config.window_decorations = "RESIZE"
config.window_frame = {
  active_titlebar_bg = "#1e2127",
  inactive_titlebar_bg = "#1e2127",
}

-- Tabs
config.tab_max_width = 50   -- maximum width in pixels
config.colors.tab_bar = {
  background = "#1e2127",  -- tab bar background

  -- inactive tabs
  inactive_tab = {
    bg_color = "#1e2127",  -- inactive tab background
    fg_color = "#839496",  -- inactive tab text color
  },

  -- active tab
  active_tab = {
    bg_color = "#26292E",   -- active tab background
    fg_color = "#f8f8f2",   -- active tab text color
  },

  -- new tab button
  new_tab = {
    bg_color = "#1e2127",
    fg_color = "#839496",
  },
}

return config
```
