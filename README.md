# My Vim Config

## Screenshots
![neovim](https://raw.githubusercontent.com/fiqgant/My-Neovim-Config/main/Screenshots/nvim1.png)

![neovim](https://raw.githubusercontent.com/fiqgant/My-Neovim-Config/main/Screenshots/nvim2.png)

![neovim](https://raw.githubusercontent.com/fiqgant/My-Neovim-Config/main/Screenshots/nvim3.png)

![neovim](https://raw.githubusercontent.com/fiqgant/My-Neovim-Config/main/Screenshots/nvim4.png)

## Plugin
- [surround.vim](http://github.com/tpope/vim-surround)
- [commentary.vim](https://github.com/tpope/vim-commentary)
- [fugitive.vim](https://github.com/tpope/vim-fugitive)
- [The NERDTree](https://github.com/preservim/nerdtree)
- [vim-airline](https://github.com/vim-airline/vim-airline)
- [vim-devicons](https://github.com/ryanoasis/vim-devicons)
- [vim-terminal](https://github.com/tc50cal/vim-terminal)
- [Awesome Vim Color Schemes](https://github.com/rafi/awesome-vim-colorschemes)
- [Tagbar](https://github.com/preservim/tagbar)
- [Bullets.vim](https://github.com/dkarter/bullets.vim)
- [fzf.vim](https://github.com/junegunn/fzf.vim)
- [fzf](https://github.com/junegunn/fzf)
- [coc.nvim](https://github.com/neoclide/coc.nvim)
- [dashboard-nvim](https://github.com/glepnir/dashboard-nvim)
- [jedi-vim](https://github.com/davidhalter/jedi-vim)
- [Copilot.vim](https://github.com/github/copilot.vim)
- [undotree](https://github.com/mbbill/undotree)
- [Semshi](https://github.com/numirias/semshi)


## General Configuration
```vim
set number
set relativenumber
set mouse=a
set autoindent
set tabstop=4
set softtabstop=4
set shiftwidth=4
set smarttab
set encoding=UTF-8
```

## NERDTree Configuration
```vim
let g:NERDTreeDirArrowExpandable="+"
let g:NERDTreeDirArrowCollapsible="~"
let g:python_highlight_all = 1

nnoremap <C-f> :NERDTreeFocus<CR>
nnoremap <C-n> :NERDTree<CR>
nnoremap <C-t> :NERDTreeToggle<CR>
nnoremap <C-l> :UndotreeToggle<CR>
nnoremap <C-l> :call CocActionAsync('jumpDefinition')<CR>
```

## Coc
```vim
:CocInstall coc-python
:CocInstall coc-javascript
:CocInstall coc-snippets
:CocCommand snippets.edit... FOR EACH FILE TYPE
```

## VIM AIRLINE CONFIGURATION
```vim
let g:airline_powerline_fonts = 1

if !exists('g:airline_symbols')
    let g:airline_symbols = {}
endif

let g:bullets_enabled_file_types = [
    \ 'markdown',
    \ 'text'
    \]

let g:airline_left_sep = ''
let g:airline_left_alt_sep = ''
let g:airline_right_sep = ''
let g:airline_right_alt_sep = ''
let g:airline_symbols.branch = ''
let g:airline_symbols.readonly = ''
let g:airline_symbols.linenr = ''
```

## Tagbar
```vim
nmap <F8> :TagbarToggle<CR>
```

## Dashboard
```vim
let g:dashboard_default_executive ='fzf'
```

## Semshi Custom Highlightss
```vim
function MyCustomHighlights()
    	hi semshiGlobal      ctermfg=blue guifg=#61afef
	hi semshiImported    ctermfg=red guifg=#d28fd7 cterm=bold gui=bold
	hi semshiBuiltin     ctermfg=yellow guifg=#f5d08b
	hi semshiSelected    ctermfg=white guifg=#dddddd ctermbg=gray guibg=#454c5a
endfunction
autocmd FileType python call MyCustomHighlights()
```
