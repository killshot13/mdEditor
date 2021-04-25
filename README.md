# mdEditor

>**v3.1.0**

## Awesome Markdown Editor/Workspace for VS Code

---

## Table of Contents

- [About](#about)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [References](#references)

---

### About <a name = "about"></a>

#### Features

- Auto-checks for errors/problems and generates a detailed output w/ references to any broken rules.

- Lints and runs autofix on save, offering auto correction/reformatting of most common errors.

- Supports the creation of `.pdf`, `.docx`, and `.html` files, which can be exported and viewed with MS Word, Adobe Acrobat, or the browser.

- Enforces syntax for any markdown flavor with a simple on/off option for every rule.

- All `html` files are linked to a basic stylesheet during creation so they look natural if viewed with the browser.

#### Details

mdEditor provides the configuration guidelines and creates the structure for an awesome VSCode Markdown editor. By creating a reusable `code-workspace`, the main portion of your IDE environment is protected from rule conflicts.

Unless you work with Markdown on a daily basis, the editor is designed to be installed locally at the user level. Markdown files can be created in the editor workspace, and existing files imported as needed for easy linting.

mdEditor is an adaptation derived from the brainchild of [Dave Johnson](https://twitter.com/thisDaveJ), which he detailed a couple years ago in [an article](https://thisdavej.com/build-an-amazing-markdown-editor-using-visual-studio-code-and-pandoc/) on his blog.

---

### Prerequisites <a name = "prerequisites"></a>

#### [Visual Studio Code](https://code.visualstudio.com/Download)

This should be self-explanantory.

#### [Pandoc](http://pandoc.org/installing.html)

This may require some guidance if you don't currently use Pandoc. I wrote a gist to help first-time users; here is [the link](https://gist.github.com/killshot13/5b379355d275e79a5cb1f03c841c7d53).

### Installation <a name = "installation"></a>

Decide where the core mdEditor files should live on your local drive (reference [About](#about) for more), then clone [mdEditor](https://github.com/killshot13/mdEditor.git) to that location.

We still need to pass the linting rulebook and Pandoc style guide to the editor workspace.

Let's install these VSCode extensions, leaving the settings at their default values.

--> [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

--> [vscode-pandoc](https://marketplace.visualstudio.com/items?itemName=DougFinke.vscode-pandoc)

Now, open mdEditor at the base directory using VSCode. Your IDE will auto-discover the `.code-workspace` file and prompt you to reopen the folder as a workspace. Confirm this choice, unless you wish to use a different configuration.

If so, there is a blank `settings.json` in the `.vscode` folder for you. Otherwise, you should disregard said folder completely.

Using this diagram, verify the file structure of your local mdEditor is free from any discrepancies.

**Tree View**
_mdEditor_
\+---.vscode
    |       `settings.json`
    |
    +---md
    |       `project1.md`
    |       `project2.md`
    |
    +---styles
    |       `style.css`
    |       `syntax.md`
    |
    |`.markdownlint.json`
    |`mdEditor.code-workspace`
    |`README.md`
    |`LICENSE`
    \---

**NOTE: On Linux you must uncomment the `pandoc.htmlOptString` in the `mdEditor.code-workspace` file. The current version, which uses Windows OS file separators, must be replaced with the Linux version; otherwise, the css styles will not be applied correctly.**

Installation is complete.
Nice job!

---

### Usage <a name = "usage"></a>

To test linting & formatting, click the `test.txt` file (in the `md` folder); it should open in the main editor window.

In the sidebar, keeping the `test.txt` tab in focus, change the filetype from `txt` to `md` and save.

Check the output in the PROBLEMS tab of your lower (terminal) panel. Several formatting violations should appear. Now make a tiny edit and save again. Most of the errors should be gone, having been corrected automatically.

To test the filetype output, enter the key combination `CTRL + K`, then press `P`. Options to create `.pdf`, `.docx`, or `.html` file should appear in the dropdown. Click each option in turn and confirm the desired result was produced.

Workspace setup is now complete and mdEditor is ready to use.

>NOTE: The `syntax.md` file in the `styles` folder contains a detailed description of the linting rules available within the editor workspace. Any rule can be toggled on/off by editing the `.markdownlint.json` file using this syntax. `"ruleID" : bool`

Happy markdown'ing! :)

[mdEditor](https://github.com/killshot13/mdEditor) is free software released under the [MIT license](https://github.com/killshot13/mdEditor/blob/main/LICENSE). Copyright 2020-2021 Michael Rehnert

### References <a name = "references"></a>

_Extensive credit is owed to [Dave Johnson](https://twitter.com/thisDaveJ) for inspiring me to create mdEditor after reading [this guide](https://thisdavej.com/build-an-amazing-markdown-editor-using-visual-studio-code-and-pandoc/) he authored._

_Additional credit and appreciation is extended to the creators, contributors, and maintainers of the following open-source software projects._

[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) is free software released under the [MIT license](https://github.com/DavidAnson/vscode-markdownlint/blob/main/LICENSE). Copyright 2015-2021 David Anson

[vscode-pandoc](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) is free software released via the VS Code marketplace. Copyright 2015-2021 Doug Finke

[Pandoc](http://johnmacfarlane.net/) is free software released under the [GPL](http://www.gnu.org/copyleft/gpl.html). Copyright 2006–2021 [John MacFarlane](http://johnmacfarlane.net/).

[VS Code](https://code.visualstudio.com/) is free software released under the [MIT license](https://github.com/microsoft/vscode/blob/main/LICENSE.txt). The project's [source code](https://github.com/microsoft/vscode/blob/main/LICENSE.txt) is available on GitHub. Copyright 2021 [Microsoft](https://www.microsoft.com/en-us/)

All software programs, extensions, plugins, and digital content referenced and/or used in the documentation and/or installation guide of mdEditor is the respective intellectual property of the creators, developers, and owners thereof and is entitled to the protections granted under U.S. Copyright law.
