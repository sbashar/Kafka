# Vim

Notes on vim.

## Commands

* ctrl + e - scroll down
* ctrl + y - scroll up
* ctrl + f - scroll down one page
* ctrl + b - scroll up one page
* H - move cursor to the top of the window
* M - move cursor to the middle of the window
* L - move cursor to the bottom of the window
* gg - go to the top of file
* G - go to the bottom of the file
* w - words
* s - sentences
* p - paragraphs
* t - tags
* a - all
* i - in
* t - till
* f - find forward
* F - find backward
* d - delete (also cut)
* c - change (delete, then place in insert mode)
* y - yank (copy)
* v - visually select
* . - repeat last command
* p - paste below
* P - paste above
* dd - delete or cut line
* yy - copy or yank line
* D/C - delete/change until end of line
* ^/$ - move to the beginning/end of line
* I/A - move to the beginning/end f line and insert
* o/O - insert new line above/below current line and insert
* mm - save the current position in the m marker
* `m - go back to the position saved using the m markter
* qa - save a macro in the a register
* q - quit saving macro
* @a - play the macro in the a register
* ~ - Toggle case to make letters capital or small.
* gt - Go to next tab
* gT - Go to previous tab
* :tabs - list all tabs including their displayed windows
* :tabm 0 - move current tab to first
* :tabm - move current tab to last
* :tabm {i} - move current tab to position i+1
* :tabn - go to next tab
* :tabp - go to previous tab
* :tabfirst - go to first tab
* :tablast - go to last tab

## Plugin Commands

### Vundle

* PluginInstall - Install plugin
* PluginUpdate - Update plugin
* PluginClean - Clean unused plugin

### Ctrlp

* Starts with ctrl + p
* ctrl + t - open code in a new tab
* ctrl + v - open code in a vertical split