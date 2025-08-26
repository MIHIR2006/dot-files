# NvChad Keybindings & Notes (Lazy.nvim Setup)

> This note includes useful default keybindings and tips for customizing them in your NvChad + Lazy.nvim setup.

---

## File Navigation & Buffers

| Keybinding   | Description                 |
|--------------|-----------------------------|
| `<Space> f f` | Find files (Telescope)      |
| `<Space> f w` | Live grep (search text)     |
| `<Space> b b` | Show open buffers           |
| `<Space> b c` | Close current buffer        |
| `<Tab>`       | Next buffer                 |
| `<S-Tab>`     | Previous buffer             |

---

## File Operations

| Keybinding   | Description                 |
|--------------|-----------------------------|
| `<Space> w`   | Save file (`:w`)            |
| `<Space> q`   | Quit window (`:q`)          |
| `<Space> n`   | Clear search highlight (`:noh`) |

---

## Plugin Management (Lazy.nvim)

| Command         | Description               |
|-----------------|---------------------------|
| `:Lazy`         | Open Lazy.nvim plugin UI  |
| `:Lazy update`  | Update installed plugins  |
| `:Lazy sync`    | Install/update plugins    |
| `:Lazy clean`   | Remove unused plugins     |

---

## File Explorer (nvim-tree)

| Keybinding   | Description               |
|--------------|---------------------------|
| `<Space> e`   | Toggle file explorer      |
| `a`           | Create new file/folder    |
| `d`           | Delete file               |
| `r`           | Rename file               |

---

## LSP & Diagnostics

| Keybinding     | Description               |
|----------------|---------------------------|
| `gd`           | Go to definition          |
| `gr`           | Go to references          |
| `K`            | Hover info (docs)         |
| `<leader> l r` | Rename symbol             |
| `<leader> l a` | Code actions              |
| `<leader> l f` | Format code               |
| `[d` / `]d`    | Previous / Next diagnostic|

---

## Commenting

| Keybinding   | Description                |
|--------------|----------------------------|
| `<Space> c`   | Toggle comment (line/block)|

---

## Additional NvChad Tips and Keybindings

- `space + t + h` : Change theme  
- `:TSInstall <language>` (e.g., elixir) : Add syntax highlighting support  
- `:TSInstallInfo` : See installed syntax highlightings  

### File Tree (Ctrl + n)

- `m` : Mark  
- `a` : Add file  
- `c` : Copy file  
- `p` : Paste file  
- `r` : Rename file  

### Search

- `space + f + f` : Find in all files  
- `space + f + b` : Find in open files (buffers)  

### Cheatsheet and Commands

- `space c h` : Show/hide cheatsheet  
- `space` (wait a second) : Command suggestions appear  
- `ctrl + h/j/k/l` : Navigation  

### Splits

- `:vsp` : Vertical split  
- `:sp` : Horizontal split  

### Other shortcuts

- `space + n` : Toggle line numbers  
- `tab` / `shift + tab` : Cycle through open buffers  
- `space + x` : Close file (buffer)  
- `space + /` : Toggle comment  
- `space + h/v` : Open terminal  
- `ctrl + ]` : Go to definition  
- `ctrl + g` : Get full path of current file  

---

## Basic Vim Movements

| Command  | Description                     |
|----------|---------------------------------|
| `0`      | Go to beginning of the line     |
| `g_`     | Go to end of the line           |
| `w`      | Move forward word by word       |
| `b`      | Move backward word by word      |
| `e`      | Go to end of the word forward   |
| `gg`     | Move cursor to first line       |
| `#G`     | Move cursor to line `#`         |
| `GG`     | Move cursor to last line        |
| `CTRL+f` | Move forward one full page      |
| `CTRL+b` | Move backward one full page     |
| `CTRL+u` | Move up half a page             |
| `CTRL+d` | Move down half a page           |
| `zt`     | Move screen so cursor is at top |
| `zb`     | Move screen so cursor is at bottom |
| `zz`     | Center screen on cursor         |
| `H`      | Move cursor to top of window    |
| `M`      | Move cursor to middle of window |
| `L`      | Move cursor to bottom of window |

---

## Terminal Usage in NvChad

- **Vertical Split:** Press `<Space> + v` to open a terminal in vertical split.  
- **Horizontal Split:** Press `<Space> + h` to open a terminal in horizontal split.  
- **Floating Terminal:** Press `<Alt> + i` to open a floating terminal window.  

### Terminal Toggling & Management

- Toggle Vertical Terminal: `<Alt> + v`  
- Toggle Horizontal Terminal: `<Alt> + h`  
- Hide Terminal: `<Leader> + K`  
- Enable Existing Terminal: `<Leader> + J`  

*Note: `<Space>` refers to the leader key (spacebar). `<Alt>` refers to the Alt key.*

---

## Custom Keybindings (in `lua/mappings.lua`)

Use this pattern to define your own keybindings:

```lua
local M = {}

M.general = {
  n = {
    ["<leader>tt"] = { "<cmd>ToggleTerm<CR>", "Toggle terminal" },
    ["<leader>n"] = { ":noh<CR>", "Clear search highlight" },
  },

  i = {
    ["jj"] = { "<Esc>", "Exit insert mode" },
  },
}

return M
