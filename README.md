# Bundler Path Helpers

These functions will automatically add and remove bundled gems and binaries
to your `$GEM_PATH` and `$PATH` respectively. They are run every time you change
directories.

## Conventions

* Your bundled gems must be stored in `vendor/bundle`
* You use `zsh`
* Your have a properly configured `$fpath`

## Installation

Go into your `zsh` dotfiles directory

  $ cd ~/.zsh

Clone the respository somewhere.

    $ git clone git://github.com/lordzork/zsh-bundler-path-helpers.git plugins/bundler-path-helpers

Alternatively, you can create a submodule.

    $ git submodule add git://github.com/lordzork/zsh-bundler-path-helpers.git plugins/bundler-path-helpers

Link the functions into your `$fpath`.

    $ ln -s plugins/bundler-path-helpers/functions/* functions/

Make sure the functions are called from the `chpwd()` function. If you don't
have `chpwd()` defined, you can use the included example.

    $ cp plugins/bundler-path-helpers/chpwd.example functions/chpwd