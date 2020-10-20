# vscode-stylefmt

[![Build Status](https://img.shields.io/travis/ronilaukkarinen/vscode-stylefmt.svg?style=flat-square)](https://travis-ci.org/ronilaukkarinen/vscode-stylefmt) [![GitHub release](https://img.shields.io/github/tag/ronilaukkarinen/vscode-stylefmt.svg?style=flat-square)](https://github.com/ronilaukkarinen/vscode-stylefmt/releases)

> [stylefmt](https://github.com/morishitter/stylefmt) is a tool that automatically formats your stylesheets.

🍴 This is a WIP fork from [mrmlnc/vscode-stylefmt](https://github.com/mrmlnc/vscode-stylefmt) which is currently obsolete. This version is in daily use and kept up to date.

## 🖌 Advantages over prettier/stylelint - why use stylefmt?

While you should definitely use [stylelint](https://stylelint.io/) for linting CSS/SCSS, for automatic formatting it's not the best solution. Prettier forces styles to certain format and it doesn't give you much options. It's tricky especially with SCSS mixins and map-gets where it may even break the formatting completely.

It's general knowledge that [stylefmt](https://github.com/morishitter/stylefmt) has not been updated since on 18 Oct 2018 which is a sad thing because basically it is just having old dependencies. However, there are still users who like to format their styles automatically and controlled with stylefmt so that's why this plugin relies on a fork of [stylefmt](https://github.com/ronilaukkarinen/stylefmt). The main goal is to keep this project active and alive.

The best thing in stylefmt is that it supports [stylelint](https://stylelint.io/) out-of-the-box without being too restrictive.

## Top contributors

This plugin is constantly kept up to date by the following persons and a bunch of [awesome contributors](https://github.com/ronilaukkarinen/vscode-stylefmt/graphs/contributors). Wanna join in development? Let us know!

| [![Roni Laukkarinen](https://avatars3.githubusercontent.com/u/1534150?v=4&s=70)](https://github.com/ronilaukkarinen) |
| --- |
| [Roni Laukkarinen](https://github.com/ronilaukkarinen) |

## Donation

Do you like this project? Support it by donating, creating an issue or pull request.

[![Donate](https://img.shields.io/badge/Donate-PayPal-green.svg)](https://paypal.me/ronilaukkarinen?locale.x=en_US)

## Install

  * Press <kbd>F1</kbd> and `select Extensions: Install Extensions`.
  * Search for and select `stylefmt`.

See the [extension installation guide](https://code.visualstudio.com/docs/editor/extension-gallery) for details.

## Usage

  * You can use global keyboard shortcut <kbd>ALT+SHIFT+F</kbd> or right-click context menu `Format code`.
  * Or press <kbd>F1</kbd> and run the command named `stylefmt: Format CSS`.

To automatically format on save, run <kbd>Cmd+Shift+P</kbd> (or <kbd>CTRL+Shift+P</kbd> on Windows systems) and select `Preferences: Open Settings (JSON)` and add this to your settings.json file:

``` json
"[scss]": {
    "editor.defaultFormatter": "ronilaukkarinen.vscode-stylefmt",
    "editor.formatOnSave": true
  },
  ```

## Supported languages

  * CSS
  * PostCSS
  * Less
  * SCSS
  * SugarSS

## Supported settings

**configBasedir**

  * Type: `string`
  * Default: `null`

Base working directory; useful for stylelint `extends` parameter.

**config**

  * Type: `object || string`
  * Default: `null`

Config object for stylelint or path to a stylelint config file.

*Will automatically look for `.stylelintrc` and `stylelint.config.js` in workspace root, or a `stylelint` param in the `package.json`, if config is omitted.*

> **Warning!**
>
> If you want to specify a file in the current directory, the path must begin with a `./` or `../` if relative to the current directory. Also you can use HOME directory as `~` symbol.

**useStylelintConfigOverrides**

  * Type: `boolean`
  * Default: `false`

Overrides rules using Stylelint plugin settings.

**showErrorMessages**

  * Type: `boolean`
  * Default: `true`

Show error messages or not. Will be automatically set to false if `editor.formatOnSave` is enabled.

## Keyboard shortcuts

For changes keyboard shortcuts, create a new rule in `File -> Preferences -> Keyboard Shortcuts`:

```json
{
  "key": "ctrl+shift+c",
  "command": "stylefmt.execute"
}
```

## Custom configuration

Read about the [stylelint rules](https://github.com/morishitter/stylefmt#stylelint-rules-that-stylefmt-can-handle) and [default rules](https://github.com/morishitter/stylefmt#default-formatting-rules-without-stylelint-config-file) in stylefmt repository.

## Changelog

See the [Releases section of our GitHub project](https://github.com/ronilaukkarinen/vscode-stylefmt/releases) for changelogs for each release version.

## License

This software is released under the terms of the MIT license.
