<img align="center" src="kittenhub.gif" />

**Feel free to hang out, explore some code, or reach out via the contact information on my Github profile.**

##### My Favorite Waiting Room Reads
1. [The Javascript Problem](https://wiki.haskell.org/The_JavaScript_Problem)
2. [ReScript – The Language After TypeScript?](https://blog.codecentric.de/en/2021/01/rescript-compare-typescript-elm)
3. [New Haskell-Based Web App Specification Language Released in Alpha](https://www.infoq.com/news/2021/01/webapp-specification-language)
4. [Build 2020 Recap](https://microsoft.github.io/react-native-windows/blog/2020/06/01/build2020recap)
5. [Top 8 JavaScript Automation Testing Frameworks In 2019](https://dev.to/arnabroychowdhury/top-8-javascript-automation-testing-frameworks-in-2019-32dk)

##### Configurations and Apps

I'm a fan of [Arc Browser](https://arc.net/). Though I've only recently started using it, it's proven to be a solid way to manage multiple contexts. I frequently switch between Github, Discord, Slack, and other platforms in my day-to-day work and find it incredibly useful.

[Neofetch](https://github.com/dylanaraps/neofetch) Results:
```txt
OS: macOS 13.5.1 22G90 arm64
Shell: fish 3.6.1
Resolution: 1728x1117
DE: Aqua
WM: Amethyst
Terminal: WezTerm
CPU: Apple M1 Pro
GPU: Apple M1 Pro
Memory: 2697MiB / 16384MiB
```

I have had a good experience with [Amethyst](https://ianyh.com/amethyst/). 
I tried [Yabai](https://github.com/koekeishiya/yabai) and a few other window managers for Mac,
but Amethyst resonates with me. It's somewhat inconsequential on smaller screens,
but if you work at a desk, it's nice to take advantage of the extra space.
Plus, I no longer need to awkwardly position windows.

As a Neovim user and a fan of Lua for programmatically configuring apps,
I really appreciate how user-friendly [WezTerm](https://github.com/wez/wezterm) is.
It's a lot snappier than [iTerm2](https://iterm2.com/),
which would sometimes freeze or experience graphical issues with Neovim tabs.

I prefer [fish](https://fishshell.com/) shell over zsh or bash for no particular reason.

```lua 
local wezterm = require 'wezterm'

-- This table will hold the configuration.
local config = {}

-- In newer versions of wezterm, use the config_builder which will
-- help provide clearer error messages
if wezterm.config_builder then config = wezterm.config_builder() end

-- This is where you actually apply your config choices

-- For example, changing the color scheme:
config.color_scheme = 'Builtin Solarized Dark'
config.font = wezterm.font 'Fisa Code'
config.window_background_opacity = 0.9

-- and finally, return the configuration to wezterm
return config
```

Here are some settings from my [Neovim](https://neovim.io/) base.lua file. I prefer not to share my exact plugins or dotfiles, 
but these are some settings that I particularly enjoy.
```lua 
-- Clear any existing autocmds in the 'ClearAutocmds' augroup
-- This is a good practice to avoid multiple autocmds being defined accidentally
vim.cmd([[
  augroup ClearAutocmds
    autocmd!
  augroup END
]])

-- Set the encoding of the script, the encoding of the file, and the fileencoding option
vim.scriptencoding = 'utf-8'
vim.opt.encoding = 'utf-8'
vim.opt.fileencoding = 'utf-8'

-- Enable line numbering
-- vim.wo.number = true
vim.opt.nu = true
vim.opt.relativenumber = true

-- Set various options for better user experience
vim.opt.title = true -- Show filename in the window title
vim.opt.autoindent = true -- Auto-indent new lines based on the previous line's indentation
vim.opt.smartindent = true -- Smart auto-indentation based on file type
vim.opt.hlsearch = false -- Highlight all search matches after search
vim.opt.incsearch = true -- Highlight matches as you type but not after
vim.opt.backup = false -- Disable creating backup files
vim.opt.showcmd = true -- Show partial command in the last line of the screen
vim.opt.cmdheight = 1 -- Set the command line height to 1
vim.opt.laststatus = 2 -- Always show the status line
vim.opt.expandtab = true -- Use spaces instead of tabs
vim.opt.scrolloff = 10 -- Keep 10 lines visible above and below the cursor
vim.opt.shell = 'zsh' -- Use zsh as the default shell
vim.opt.backupskip = {'/tmp/*', '/private/tmp/*'} -- Skip creating backups for these directories
vim.opt.inccommand = 'split' -- Show the effects of a command incrementally, in a split window
vim.opt.ignorecase = true -- Case insensitive searching unless /C or capital letter in search

-- More options for improved user experience
vim.opt.smarttab = true -- Use smart tabs for indent and tab completion
vim.opt.breakindent = true -- Keep indentation when wrapping long lines
vim.opt.shiftwidth = 2 -- Set the number of spaces per indentation level
vim.opt.tabstop = 2 -- Set the number of spaces per tab character
vim.opt.wrap = false -- Disable line wrapping
vim.opt.backspace = {'start', 'eol', 'indent'} -- Allow backspace in insert mode to delete characters

-- Set options related to searching and file navigation
vim.opt.path:append{'**'} -- Search down into subfolders when using :find command
vim.opt.wildignore:append{'*/node_modules/*'} -- Ignore 'node_modules' folder when using file-related commands

-- Configure undercurl for better visual feedback on spelling errors
vim.cmd([[let &t_Cs = "\e[4:3m"]]) -- Set the terminal code for the start of undercurl
vim.cmd([[let &t_Ce = "\e[4:0m"]]) -- Set the terminal code for the end of undercurl

-- Turn off paste mode when leaving insert mode
vim.api.nvim_exec([[
  autocmd InsertLeave * set nopaste
]], false)

-- Add asterisks when formatting block comments
vim.opt.formatoptions:append{'r'}

-- UFO fold config (requires ufo plugin)
vim.o.foldcolumn = '1' -- '0' is not bad
vim.o.foldlevel = 99 -- Using ufo provider need a large value, feel free to decrease the value
vim.o.foldlevelstart = 99
vim.o.foldenable = true
```

##### Caffeine (Mostly Coffee) 

My daily drivers, though I have more gear:

  - Rocket Appartamento
  - Clever Dripper 
  - [Aeropress usually inverted method temps vary by bean](https://aeropress.com/)
  - [(Yerba Mate) Guayaki Canned](https://guayaki.com/)
  - [(Yerba Mate) Union Suave Loose Leaf at 72c](https://www.yerbamatelab.com/union-suave-yerba-mate-review/)
