# summerfruit256.nvim

![Screenshot](https://github.com/user-attachments/assets/9d0878e0-b4bc-413b-a69b-f1b71458bb5b)

This is a fork of https://github.com/vim-scripts/summerfruit256.vim to make it
work in recent (as of 2025, i.e. 0.10+) versions of Neovim.

So far, this is done by just restoring the original Vim color definitions as
recommended in the `:help colorscheme` docs.

## Additional configuration you may require

Below are some other issues that made the scheme look different from how it
was before in _my_ setup, but as these may not occur in yours (e.g. because
you've always used the Vim GUI or only started using Vim at a version greater
than 9.1.0061), I didn't put them into the theme file itself.

### Colors are less saturated

![Desaturated colors](https://github.com/user-attachments/assets/5a479a02-d757-40fd-a36c-74ff89593d06)

If the colors look a bit less saturated than you're used to from Vim or older
versions of Neovim, you may also need to `:set notermguicolors`, because Neovim
changed something related to that as well (too lazy to figure out exactly what
& don't care).

### Visual selections aren't syntax highlighted

![Visual selection with black text color](https://github.com/user-attachments/assets/71f0cf74-73f2-40a6-bde7-8b00e1673dc6)

This was actually [changed in Vim itself](https://github.com/vim/vim/commit/e6d8b4662ddf9356da53f56e363b67b524fd8825)
starting at version 9.1.0061 and Neovim just adopted it. You may also notice
that the selection's background color is darker than in older versions.

To fix this, just do `:highlight Visual ctermfg=NONE ctermbg=LightGrey`
or the equivalent for GUI colors (`guifg`, `guibg`) if you do want to use them.

After that, it should go back to looking like this:

![Visual selection with syntax highlighting](https://github.com/user-attachments/assets/53879448-be7f-4a47-90d0-1975c8919bb5)

# Original README of the summerfruit256.vim repo

This is a mirror of http://www.vim.org/scripts/script.php?script_id=2577

88/256 color version of Armin Ronacher's summerfruit color scheme (vimscript #1872).  Used Henry So Jr.'s color approximation (vimscript #1243) for the color conversion.

You can find a screenshot on http://www.mabae.de/2008/02/09/summerfruit-vim-color-scheme-in-256-colors/
