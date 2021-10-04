# 🚪better-escape.nvim

This is a lua version of
[better_escape.vim](https://github.com/jdhao/better-escape.vim)

✨Features
--------
* Escape without getting delay when typing in insert mode
* Customizable mapping and timeout
* Use multiple mappings
* Really small and fast

📦Installation
------------
Use your favourite package manager and call the setup function.
```lua
-- lua with packer.nvim
use {
  "max397574/better-escape.nvim",
  config = function()
    require("better_escape").setup()
  end,
}
```

⚙️Customization
-------------
Call the setup function with your options as arguments.

```lua
-- lua, default settings
require("better_escape").setup {
    mapping = {"jk", "jj"}, -- a table with mappings to use
    timeout = vim.o.timeoutlen, -- the time in which the keys must be hit in ms. Use option timeoutlen by default
    clear_empty_lines = false, -- clear line after escaping if ther is only whitespace
    keys = "<Esc>", -- keys used for escaping, if it is a function will use the result everytime
    -- example
    -- keys = function()
    --   return vim.fn.col '.' - 2 >= 1 and '<esc>l' or '<esc>'
    -- end,
}
```

👀Demo
------

### `inoremap jk <ESC>`:

https://user-images.githubusercontent.com/81827001/134317521-0c446238-c24c-4303-9539-e5eb6236d221.mp4

### better-escape.nvim:

https://user-images.githubusercontent.com/81827001/134317540-95a66237-dd77-49a9-8f11-8b037458354c.mp4

