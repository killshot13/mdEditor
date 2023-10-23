# **Change Log** 📜📝

All notable changes to _mdEditor_ will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

---

## [**v2.0.0**] - 2023-10-23

MAJOR VERSION UPDATE

### Added

* New `.markdownlintignore` file ensures `mdEditor` only lints and formats markdown files within the `md/` directory, rather than the entire workspace

* All options/values seen in the snippet below were added to the workspace settings

> ```json
>  "[markdown]": {
>	  "diffEditor.ignoreTrimWhitespace": false,
>	  "editor.codeActionsOnSave": {
>		  "source.fixAll.markdownlint": true
>	  },
>	  "editor.formatOnPaste": false,
>	  "editor.semanticHighlighting.enabled": true,
>	  "editor.unicodeHighlight.ambiguousCharacters": false,
>	  "editor.unicodeHighlight.invisibleCharacters": false,
>  },
>  "markdown.updateLinksOnFileMove.enabled": "prompt",
> ```

### Changed

* BREAKING CHANGE: Removed support for the [now deprecated](https://marketplace.visualstudio.com/items?itemName=DougFinke.vscode-pandoc) `vs-code-pandoc`, formerly maintained by Doug Finke
* BREAKING CHANGE: Migrated to a [direct fork](https://marketplace.visualstudio.com/items?itemName=ChrisChinchilla.vscode-pandoc) of `vs-code-pandoc` actively maintained by Chris Chinchilla
* BREAKING CHANGE: `mdEditor.code-workspace` now sets the `markdown.validate.enabled` option to `false` by default. This disables Vs Code's native Markdown validation in favor of the linting and formatting options that `mdEditor` provides. To revert this change, delete line 31 from `mdEditor.code-workspace`.
* Renamed the linting rules reference document
 `styles/syntax.md` to `styles/rules.md` to align with the `markdownlint` file from which it was derived

### Improved

* Edited the linting rules reference document `styles/rules.md` (formerly `styles/syntax.md`) to reflect the rules in the latest `markdownlint` version (v0.31.1)

### Removed

* Deleted unused `.gitignore` file

---

## [**v1.1.0**] - 2021-06-28

MINOR VERSION UPDATE

### Added (1.1.0)

* mdEditor will now ask if you want to install the recommended extensions. The prompt should appear when entering the workplace after install. If you already have them, don't worry, that's why nothing showed up

### Changed (1.1.0)

```json
"MD003": { "style": "atx" }
```

* Enforces `atx` styling rule (MD003) by adding the above line to `.markdownlint.json` to alleviate editor conflicts

### Improved (1.1.0)

* Added two separate lines in the Workspace configuration, one to support the Windows file system, and one to support Linux. The config is in "Windows mode" by default However, all you need to switch is to cautiously copy & paste the Linux snippet exactly where the Windows snippet is, then do the opposite for the Windows one

---

## [**v1.0.0**] - 2021-04-19

INITIAL PUBLIC RELEASE

### Added (1.0.0)

* docs(_mdEditor_): contrib guide & pre-release fixes by @killshot13 in <https://github.com/killshot13/mdEditor/pull/8>
* Development branch added by @killshot13 in <https://github.com/killshot13/mdEditor/pull/9>

### Changed (1.0.0)

* [ImgBot] Optimize images by @imgbot in <https://github.com/killshot13/mdEditor/pull/1>
* [ImgBot] Optimize images by @imgbot in <https://github.com/killshot13/mdEditor/pull/2>
* Test: image #1 responsive placement by @killshot13 in <https://github.com/killshot13/mdEditor/pull/3>
* [ImgBot] Optimize images by @imgbot in <https://github.com/killshot13/mdEditor/pull/7>

### Fixed (1.0.0)

* mdEditor README.md fix by @killshot13 in <https://github.com/killshot13/mdEditor/pull/4>
* mdEditor README.md fix by @killshot13 in <https://github.com/killshot13/mdEditor/pull/6>

#### New Contributors (1.0.0)

* @imgbot made their first contribution in <https://github.com/killshot13/mdEditor/pull/1>
* @killshot13 made their first contribution in <https://github.com/killshot13/mdEditor/pull/3>

**Full Changelog (1.0.0)** <https://github.com/killshot13/mdEditor/commits/v1.0.0>
