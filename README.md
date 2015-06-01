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
- Clone both the [thoughtbot's
dotfiles](http://www.github.com/thoughtbot/dotfiles) and this repo to your home
directory (or other directory of your choosing).
- You edit `gitconfig` to set your own user and email.
- Install the `rcm` dotfile management utility: https://github.com/thoughtbot/rcm
- Run the `rcup` utility to symlink your dotfiles to your home directory:
-- If you cloned the dotfile repos to `$HOME` you can run:
`env RCRC=$HOME/dotfiles/rcrc rcup`
-- Otherwise you'll need to specify the specific folder that has your dotfiles
and which files to exclude:
`EXCLUDES="README.md LICENSE" DOTFILES_DIRS="$HOME/dotfiles-local $HOME/dotfiles" rcup`
