# Dotfiles

These are my additions to [thoughtbot's
dotfiles](http://www.github.com/thoughtbot/dotfiles)

## Installation

Use these in combination with another set of dotfiles (such as thoughtbot's)
that load `.local` versions of themselves. Symlink both sets of dotfiles to your
root directory.

The easiest way to maintain this system is to use the
[`rcm`](http://www.github.com/thoughtbot/rcm) command-line utility

Here's what you need to do:

1. Clone both the [thoughtbot's
dotfiles](http://www.github.com/thoughtbot/dotfiles) and this repo to your home
directory (or other directory of your choosing).
2. You edit `gitconfig` to set your own user and email.
3. Install the `rcm` dotfile management utility: https://github.com/thoughtbot/rcm
4. Run the `rcup` utility to symlink your dotfiles to your home directory:
  - If you cloned the dotfile repos to `$HOME` you can run:
`env RCRC=$HOME/dotfiles/rcrc rcup`
  - Otherwise you'll need to specify the specific folder that has your dotfiles
and which files to exclude:
`EXCLUDES="README.md LICENSE" DOTFILES_DIRS="/path/to/dotfiles-local /path/to/dotfiles" rcup`

Note that `curl` needs to be installed for the `rcup` utility to work correctly
(I ran into an issue with this on a new Ubuntu 15.04 virtual machine install).

My git alias `g` uses `unbuffer` which on Ubuntu requires 
`sudo apt-get install expect-dev`

## Terminal colors

These are the terminal color configurations I use to go with the gruvbox VIM 
color schme. On my to do list for my dotfiles would be to make these a script.

Foreground: ffffff
Background: 333233 (seems like 252525 is what works on Ubuntu gnome-terminal..)
Bold: d3d7cf
Selection: c1ddff
Cursor: c7c7c7
Cursor text: ffffff

Black dark: 2d3436
Black light: 555753
Red dark: cc1c01
Red light: ef2929
Green 4e9a06 8ae233
Yellow c4a003 fce94f
Blue 3465a4 729fcf
Magenta 75507b ad7fa8
Cyan 07989a 32e2e2
White d3d7cf eeeeec
