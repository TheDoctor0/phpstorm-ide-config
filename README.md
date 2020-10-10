# PhpStorm IDE configuration [![PhpStorm version](https://img.shields.io/badge/PhpStorm-2020.1.2-brightgreen.svg)](https://www.jetbrains.com/phpstorm/) [![License](https://img.shields.io/github/license/TheDoctor0/phpstorm-ide-config)](https://github.com/TheDoctor0/phpstorm-ide-config/blob/master/LICENSE.md)

This is my global configuration for [PhpStorm](https://www.jetbrains.com/phpstorm/).
It contains custom configs for code styling, keymaps, inspections as well as some file templates.
I use Git to track these files and to synchronize them between workstations - Windows and macOS.

There is also cheat sheet for my personalized PhpStorm keymap, available [online](https://thedoctor0.github.io/phpstorm-ide-config/) or as [PDF](https://github.com/TheDoctor0/phpstorm-ide-config/blob/master/phpstorm-cheat-sheet.pdf).

Feel free to use or fork this repository.

## Content

Directory     | Contents
--------------|---------
codestyles    | Code Style settings (Editor > Code Style)
colors        | Colors & Fonts settings (Editor > Colors & Fonts)
fileTemplates | File and Code Templates (Editor > File and Code Templates)
inspection    | Inspection profiles (Editor > Inspections)
keymaps       | Keyboard shortcuts (Keymap)
templates     | Live templates (Editor > Live Templates)

## Code Style

Language            | Standards
--------------------|---------
PHP                 | 4 spaces, [PSR-2](http://www.php-fig.org/psr/psr-2/) + [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) + personal preferences
Javascript / Vue.js | 2 spaces
HTML / Twig         | 4 spaces
CSS / SCSS / LESS   | 2 spaces
Yaml                | 2 spaces

## Installation

Warning: Before you do this, make sure PhpStorm is not running, or it will overwrite the changed files before shutting down.

Use the following commands to go to the config directory, remove default directories and files, and pull the configuration from repository:

```bash
# Replace with the actual directory name, depending on OS and PhpStorm version (see below for help).
cd ~/.PhpStorm2020.1.2/config
# It will be path with jba_config if you are using settings synchronization with JetBrains account.
cd ~/.PhpStorm2020.1.2/config/jba_config

rm -r codestyles colors fileTemplates inspection keymaps templates options
rm editor.codeinsight.xml options/colors.scheme.xml options/editor.xml options/ide.general.xml options/keymap.xml options/material_custom_theme.xml options/material_theme.xml

git init
git remote add origin git@github.com:TheDoctor0/phpstorm-ide-config.git
git fetch
git checkout -t origin/master
```

### Location of the config folder

OS      | Location
--------|---------
Windows | `%APPDATA%\JetBrains\.PhpStorm2020.1.2`
Linux   | `~/JetBrains/.PhpStorm2020.1.2`
macOS   | `~/Library/Application Support/JetBrains/PhpStorm2020.1.2`

See [Default IDE directories](https://www.jetbrains.com/help/phpstorm/tuning-the-ide.html#default-dirs) for more information about the location of the configuration directory.

## Shortcuts

### General
Shortcut                | Action
------------------------|----------------------------------
Ctrl + Tab              | Show switcher
Ctrl + E                | Show last files
Alt + R                 | Recent projects dialog
Ctrl + Shift + E        | Show recent locations
Ctrl + Space            | Show hinting dialog
Alt + Enter             | Show intention actions
Ctrl + Shift + Enter    | Complete current statement
Ctrl + J                | Show available live templates
Ctrl + Shift + V        | Select to paste from clipboards
Alt + Click             | Multiple cursors
Ctrl + Alt + S          | Open settings

### Miscellaneous
Shortcut                | Action
------------------------|----------------------------------
Ctrl + Ctrl             | Run anything
Shift + F10             | Run current configuration
Alt + Shift + F10       | Run configuration dialog
Alt + S                 | New scratch file
Alt + Home + Alt + Insert | New file in specified location
Ctrl + Alt + Shift + C  | Copy reference
Shift + F4              | Close other tabs
Alt + Left              | Move to previous tab
Alt + Right             | Move to next tab
Ctrl + ,                | Split vertically
Ctrl + Shift + ,        | Remove split

### Search / Replace
Shortcut                | Action
------------------------|----------------------------------
Shift + Shift           | Search everywhere
Ctrl + Shift + A        | Find action
Ctrl + N                | Find class
Ctrl + Shift + N        | Find file
Ctrl + F                | Find in file
Ctrl + Shift + F        | Find globally
Ctrl + R                | Replace in file
Ctrl + Shift + R        | Replace globally
Ctrl + Shift + F7       | Highlight usages in this file
Ctrl + Alt + Shift + I	| Run inspection by name

### Navigation
Shortcut                | Action
------------------------|----------------------------------
Ctrl + Alt + Right      | Next edit location
Ctrl + Alt + Left       | Previous edit location
Ctrl + G                | Go to line : column
Ctrl + Right            | Move caret to next word
Ctrl + Left             | Move caret to previous word
Ctrl + Shift + Up       | Move line or selection up
Ctrl + Shift + Down     | Move line or selection down
Alt + Down              | Next method
Alt + Up                | Previous method
F2                      | Next error
Shift + F2              | Previous error
Ctrl + Shift + M        | Move between matching braces
Ctrl + [                | Move to block start
Ctrl + ]                | Move to block end
Ctrl + Alt + Page Up    | Clone caret above
Ctrl + Alt + Page Down  | Clone caret below
Ctrl + Home             | Go to the start of file
Ctrl + End              | Go to the end of file

### Selection
Shortcut                | Action
------------------------|----------------------------------
Ctrl + Alt + W          | Select line at caret
Ctrl + W                | Extend selection
Ctrl+ Shift + W         | Shrink selection
Ctrl + Shift + O        | Select all occurrences
Alt + J                 | Add selection for next occurrence
Ctrl + Shift + Left     | Add previous word to selection
Ctrl + Shift + Right    | Add next word to selection
Ctrl + Alt + Up         | Previous highlighted occurrence
Ctrl + Alt + Down       | Next highlighted occurrence
Shift + Home            | Select all to the start of line
Shift + End             | Select all to the end of line
Alt + /                 | Cyclic expand word from next
Shift + Alt + /         | Cyclic expand word from previous
Ctrl + Shift + [        | Move to block start with selection
Ctrl + Shift + ]        | Move to block end with selection
Alt + Shift + [	        | Move caret backwards a paragraph with selection
Ctrl + Shift + ]	    | Move caret forwards a paragraph with selection
Alt + H                 | Highlight current scope
Alt + F1	            | Select In dialog

### Coding
Shortcut                | Action
------------------------|----------------------------------
Alt + Insert            | Generate code dialog
Ctrl + O                | Override method
Ctrl + I                | Implement method
Alt + L                 | Reformat code
Alt + Shift + L         | Reformat code dialog
Ctrl + Alt + I          | Auto-indent line or selection
Ctrl + D                | Duplicate line or selection
Ctrl + Shift + D        | Duplicate whole line
Ctrl + Y                | Delete line at caret
Ctrl + Shift + Y        | Delete to the line end
Ctrl + Backspace        | Delete previous word
Ctrl + Enter            | Split string to next line
Ctrl + Shift + J        | Join lines
Shift + Enter           | Start new line
Ctrl + /                | Comment line or selection
Ctrl + =                | Expand
Ctrl + -                | Collapse

### Documentation
Shortcut                | Action
------------------------|----------------------------------
Ctrl + B                | Show declaration / usage
Ctrl + Alt + B          | Show implementation(s)
Ctrl + Shift + B        | Show type declaration
Ctrl + F12              | Show file structure
Ctrl + H                | Show type hierarchy
Ctrl + Alt + H          | Show method hierarchy
Ctrl + Shift + H        | Show call hierarchy
Ctrl + Shift + I        | Show quick definition
Ctrl + Q                | Show quick documentation
Ctrl + P                | Show parameter info
Shift + F1              | Show documentation on php.net

### Refactoring
Shortcut                | Action
------------------------|----------------------------------
Ctrl + Alt + R          | Show refactor dialog
Ctrl + Alt + V          | Extract variable
Ctrl + Alt + C          | Extract constant
Ctrl + Alt + P          | Extract parameter
Ctrl + Alt + F          | Extract field
Ctrl + Alt + M          | Extract method
F6                      | Move
Shift + F6              | Rename
Ctrl + Alt + T          | Surround with dialog
Ctrl + Shift + Delete   | Unwrap
Ctrl + Shift + U        | Toggle case

### Tools
Shortcut                | Action
------------------------|----------------------------------
Alt + F1                | Show tools dialog
Alt + 0                 | Terminal
Alt + 1                 | Project
Alt + 3                 | Hierarchy
Alt + 4                 | Run
Alt + 6                 | Database
Alt + 8                 | Remote host
Alt + 9                 | Version control
Shift + Escape          | Hide active tool
Ctrl + Shift + '        | Expand / Shrink tool window
Ctrl + Shift + Q        | Start SSH session
Alt + U                 | Upload to default server

### VCS
Shortcut                | Action
------------------------|----------------------------------
Alt + `                 | Show operations dialog
Ctrl + Shift + `        | Show branches dialog
Alt + G                 | Show shelve dialog
Ctrl + L                | Local history
Ctrl + Shift + L        | Local history for selection
Ctrl + T                | Update project
Ctrl + K                | Commit
Ctrl + Shift + K        | Push
Ctrl + Alt + A          | Add
Ctrl + Alt + Z          | Revert
Alt + Shift + U         | Shelve changes
