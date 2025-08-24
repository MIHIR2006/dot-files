# NvChad Keybindings & Notes (Lazy.nvim Setup)

> This note includes useful default keybindings and tips for customizing them in your NvChad + Lazy.nvim setup.

---

## File Navigation & Buffers

| Keybinding       | Description                      |
|------------------|----------------------------------|
| `<Space> f f`     | Find files (Telescope)          |
| `<Space> f w`     | Live grep (search text)         |
| `<Space> b b`     | Show open buffers               |
| `<Space> b c`     | Close current buffer            |
| `<Tab>`           | Next buffer                     |
| `<S-Tab>`         | Previous buffer                 |

---

## File Operations

| Keybinding       | Description                      |
|------------------|----------------------------------|
| `<Space> w`       | Save file (`:w`)                |
| `<Space> q`       | Quit window (`:q`)              |
| `<Space> n`       | Clear search highlight (`:noh`) |

---

## Plugin Management (Lazy.nvim)

| Command           | Description                      |
|------------------|----------------------------------|
| `:Lazy`           | Open Lazy.nvim plugin UI         |
| `:Lazy update`    | Update installed plugins         |
| `:Lazy sync`      | Install/update plugins           |
| `:Lazy clean`     | Remove unused plugins            |

---

## File Explorer (nvim-tree)

| Keybinding       | Description                      |
|------------------|----------------------------------|
| `<Space> e`       | Toggle file explorer            |
| `a`               | Create new file/folder          |
| `d`               | Delete file                     |
| `r`               | Rename file                     |

---

## LSP & Diagnostics

| Keybinding         | Description                      |
|--------------------|----------------------------------|
| `gd`               | Go to definition                 |
| `gr`               | Go to references                 |
| `K`                | Hover info (docs)                |
| `<leader> l r`     | Rename symbol                    |
| `<leader> l a`     | Code actions                     |
| `<leader> l f`     | Format code                      |
| `[d` / `]d`        | Prev / Next diagnostic           |

---

## Commenting

| Keybinding       | Description                      |
|------------------|----------------------------------|
| `<Space> c`       | Toggle comment (line/block)     |

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
