# cheat #

Cheat manages text-only cheat sheets from git sources. It syncs them via git
checkout/pull, displays them, and lets you grep them.

## Config ##

Sources are defined in `~/.config/cheat/config`, one github repository per line.
If the sheets are located in a subdirectory, add the path after a `|`.

Example:

```
https://github.com/ticki/sheets.git
https://github.com/chrisallenlane/cheat.git|cheat/cheatsheets
```

**Note:** Later entries will win a cheat sheet name collision.

## Usage ##

```sh
cheat -h        # Usage information. Also --help.
cheat -s        # Sync cheat sources from git repos. Also --sync.
cheat -l        # List cheat sheets. Also --list
cheat ascii     # Print a cheat sheet
cheat -g ascii  # Grep sheets for "ascii". Also --grep.
```

## Autocompletion ##

### zsh ###

```
compdef '_files -W "$HOME/.config/cheat/sheets"' cheat
```

### bash ###

TODO
