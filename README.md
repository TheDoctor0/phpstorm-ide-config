# PhpStorm IDE configuration

[![PhpStorm version](https://img.shields.io/badge/PhpStorm-2019.2-brightgreen.svg)](https://www.jetbrains.com/phpstorm/)
[![License](https://img.shields.io/github/license/TheDoctor0/phpstorm-ide-config.svg)](https://github.com/TheDoctor0/phpstorm-ide-config/blob/master/LICENSE.md)

This is my global configuration for [PHPStorm](https://www.jetbrains.com/phpstorm/).
It contains custom configs for code styling, keymaps, inspections as well as some file templates.
I use Git to track these files and to synchronize them between workstations - Windows and MacOS.

Feel free to use or fork this repository.

## Content

Directory | Contents
----------|---------
codestyles | Code Style settings (Editor > Code Style)
colors | Colors & Fonts settings (Editor > Colors & Fonts)
fileTemplates | File and Code Templates (Editor > File and Code Templates)
inspection | Inspection profiles (Editor > Inspections)
keymaps | Keyboard shortcuts (Keymap)
templates | Live templates (Editor > Live Templates)

## Code Style

Language            | Standards
--------------------|---------
PHP                 | 4 spaces, [PSR-2](http://www.php-fig.org/psr/psr-2/) + [PSR-12](https://github.com/php-fig/fig-standards/blob/master/proposed/extended-coding-style-guide.md) + personal preferences
Javascript / Vue.js | 2 spaces
HTML / Twig         | 4 spaces
CSS / SCSS / LESS   | 2 spaces
Yaml                | 2 spaces

## Installation

Before you do this, make sure PhpStorm is not running, or it will overwrite the changed files before shutting down.
Use the following commands to go to the config directory, remove some default directories, and pull the files from my repository:

```bash
# replace with the actual directory name, depending on OS and PhpStorm version (see below).
cd ~/.PhpStorm2019.2/config

# remove the files and folders that are in this repository
rm -r colors codestyles fileTemplates inspection keymaps templates

git init
git remote add origin git@github.com:TheDoctor0/phpstorm-ide-config.git
git fetch
git checkout -t origin/master
```

### Location of the config folder

OS | Location
---|---------
Windows | `C:\Users\<User name>\.PhpStorm2019.2\config`
Linux | `~/.PhpStorm2019.2/config`
OS X | `~/Library/Preferences/PhpStorm2019.2`

See [Default IDE directories](https://www.jetbrains.com/help/phpstorm/tuning-the-ide.html#default-dirs) for more information about the location of the configuration directory.