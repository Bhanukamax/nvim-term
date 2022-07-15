# Neovim Terminal Manager


## Introduction

This plugin allows to easily manage a terminal buffer within neovim.

#### How to install

- If you are using `Plug` add the plug to your plugin list:
```
Plug 'nvim-lua/plenary.nvim' " don't forget to add this one if you don't have it yet!
Plug 'ThePrimeagen/harpoon'
Plug 'Bhanukamax/neotermman',  { 'branch': 'feat/toggle' }

```

- resource the vimrc
```
:source $MYVIMRC
```

- run plug install
```
:PlugInstall
```

### Features:

- Opens a terminal buffer and make it unlisted so it won't come accrose when you move between buffers using `:bn` or `:bp`
- Always opens the same terminal buffer provided you don't quite the terminal.


### Methods

- OpenTerm() - opens the terminal buffer in the current window
- OpenFloatingTerm - opens the terminal buffer in a new floating window
- Pressing `q` will close the term buffer

```
nnoremap <leader>T :call OpenTerm()<CR>
nnoremap <leader>t :call OpenFloatingTerm()<CR>
```


### Caveats

This plugin opens the first terminal buffer found on the buffer list including unlisted buffers (can be found by executing `:ls!`, so if you are having multiple terminal buffers this plugin will always only open the first one.
