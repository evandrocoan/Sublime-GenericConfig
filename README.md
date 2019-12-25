Sublime-GenericConfig
=====================

Sublime-GenericConfig adds syntax highlighting of the configuration files
to Sublime Text 2 and Sublime Text 3.

It aims to provide generic highlighting for files which are
not supported by other plugins (for example ini files, nginx config).

This plugin may be used for a wide range of configuration files
because highlighting is based on common syntax constructions.

*NOTE*: `0.0.6` is last version for Sublime Text 2.


## Installation

### By Package Control

1. Download & Install **`Sublime Text 3`** (https://www.sublimetext.com/3)
1. Go to the menu **`Tools -> Install Package Control`**, then,
   wait few seconds until the installation finishes up
1. Now,
   Go to the menu **`Preferences -> Package Control`**
1. Type **`Add Channel`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   input the following address and press <kbd>Enter</kbd>
   ```
   https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json
   ```
1. Go to the menu **`Tools -> Command Palette...
   (Ctrl+Shift+P)`**
1. Type **`Preferences:
   Package Control Settings – User`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
   find the following setting on your **`Package Control.sublime-settings`** file:
   ```js
       "channels":
       [
           "https://packagecontrol.io/channel_v3.json",
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
       ],
   ```
1. And,
   change it to the following, i.e.,
   put the **`https://raw.githubusercontent...`** line as first:
   ```js
       "channels":
       [
           "https://raw.githubusercontent.com/evandrocoan/StudioChannel/master/channel.json",
           "https://packagecontrol.io/channel_v3.json",
       ],
   ```
   * The **`https://raw.githubusercontent...`** line must to be added before the **`https://packagecontrol.io...`** one, otherwise,
     you will not install this forked version of the package,
     but the original available on the Package Control default channel **`https://packagecontrol.io...`**
1. Now,
   go to the menu **`Preferences -> Package Control`**
1. Type **`Install Package`** on the opened quick panel and press <kbd>Enter</kbd>
1. Then,
search for **`GenericConfig`** and press <kbd>Enter</kbd>

See also:

1. [ITE - Integrated Toolset Environment](https://github.com/evandrocoan/ITE)
1. [Package control docs](https://packagecontrol.io/docs/usage) for details.


Supported constructions
-----------------------

* One line comments (`#`, `//`, `--` and `;`)
* Numbers, hex values, numbers with units (`12M`, `10kHz` etc)
* Color (`#ccc`, `#12ccff` etc)
* Common constants (`true`/`false`, `yes`/`no` etc)
* Strings (single quotes and double quoted)
* Sections (`[name]`, `<name>`, `name { ... }`)
* Key-value constructions (`key = value`, `key: value`, `key value ...`)
* Variables (`$name`, `%name`, `%name%`, `${name}` and few others)
* Uppercase names (`SOME_NAME`)
* URL-like strings (`http://name.org`, `some://name:port/path`)
* RegEx-like strings (`^...$`)
* Common operators (`+`, `-` etc)
* Mime-like strings (`image/gif`, `multipart/form-data` etc)
* Function call (`name()`)
