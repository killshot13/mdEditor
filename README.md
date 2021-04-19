# mdEditor

> **Awesome Markdown Editor/Workspace for VS Code**
>
> **v3.0.0**

## Table of Contents

- [About](#about)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [References](#references)

## About <a name = "about"></a>

### Features

<a href="https://github.com/killshot13/mdEditor"><img align="right" width="605" height="395" src="https://github.com/killshot13/mdEditor/blob/main/images/markdown-to-html.jpg" alt="HTML file created with mdEditor"></a>

- Auto-checks for errors/problems and generates a detailed output for any broken rules.

- Lints and runs autofix on save which will correct/reformat most common errors.

- Supports the creation of `.pdf`, `.docx`, and `.html` files, which can be exported and viewed with MS Word, Adobe Acrobat, or the browser.

- Enforces syntax for any markdown flavor with a simple on/off option for every rule.

- All `html` files are linked to a basic stylesheet during creation so they look natural if viewed with the browser.

### Details

mdEditor provides the configuration guidelines and creates the structure for an awesome VSCode Markdown editor. By creating a reusable `code-workspace`, the main portion of your IDE environment is protected from rule conflicts.

Unless you work with Markdown on a daily basis, the editor is designed to be installed locally at the user level.Markdown files can be created in the editor workspace, and existing files imported as needed for easy linting.

mdEditor is an adaptation derived from the brainchild of [Dave Johnson](https://twitter.com/thisDaveJ), which he detailed a couple years ago in [an article](https://thisdavej.com/build-an-amazing-markdown-editor-using-visual-studio-code-and-pandoc/) on his blog.

---

<p align="center">
    <a href="https://github.com/killshot13/mdEditor"><img width="1080" height="607.5" src="https://github.com/killshot13/mdEditor/blob/main/images/mdEditor.gif" alt="GIF file showing how mdEditor works"></a>
</p>

## Prerequisites <a name = "prerequisites"></a>

[Visual Studio Code](https://code.visualstudio.com/Download)
This should be self-explanantory.

[Pandoc](http://pandoc.org/installing.html)
Used to transform Markdown into `.pdf`, `.docx`, and `.html` files.

## Installation <a name = "installation"></a>

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

Installation is complete.
Nice job!

## Usage <a name = "usage"></a>

To test linting & formatting, click the `test.txt` file (in the `md` folder); it should open in the main editor window.

In the sidebar, keeping the `test.txt` tab in focus, change the filetype from `txt` to `md` and save.

Check the output in the PROBLEMS tab of your lower (terminal) panel. Several formatting violations should appear. Now make a tiny edit and save again. Most of the errors should be gone, having been corrected automatically.

To test the filetype output, enter the key combination `CTRL + K`, then press `P`. Options to create `.pdf`, `.docx`, or `.html` file should appear in the dropdown. Click each option in turn and confirm the desired result was produced.

Workspace setup is now complete and mdEditor is ready to use.

>NOTE: The `syntax.md` file in the `styles` folder contains a detailed description of the linting rules available within the editor workspace. Any rule can be toggled on/off by editing the `.markdownlint.json` file using this syntax. `"ruleID" : bool`

Happy markdown'ing! :)

## References <a name = "references"></a>

<a href="https://github.com/killshot13/mdEditor"><img align="left" width="605" height="395" src="https://github.com/killshot13/mdEditor/blob/main/images/markdown-to-docx.jpg" alt="DOCX file created with mdEditor"></a>

_Credit is owed to [Dave Johnson](https://twitter.com/thisDaveJ) for inspiring me to create mdEditor after reading [this guide](https://thisdavej.com/build-an-amazing-markdown-editor-using-visual-studio-code-and-pandoc/)  he authored._

[mdEditor](https://github.com/killshot13/mdEditor) is free software released under the [MIT license](https://github.com/killshot13/mdEditor/blob/main/LICENSE) Copyright 2020-2021 Michael Rehnert

[Pandoc](http://johnmacfarlane.net/) is free software released under the [GPL](http://www.gnu.org/copyleft/gpl.html). Copyright 2006–2021 [John MacFarlane](http://johnmacfarlane.net/).

[VS Code](https://code.visualstudio.com/) is free software released under the [MIT license](https://github.com/microsoft/vscode/blob/main/LICENSE.txt). The project's [source code](https://github.com/microsoft/vscode/blob/main/LICENSE.txt) is available on GitHub. Copyright 2021 [Microsoft](https://www.microsoft.com/en-us/)

**All VS Code extensions, software programs, and digital content referenced and/or used in the documentation and/or installation guide of mdEditor is the respective intellectual property of the creators, developers, and owners thereof. All applicable copyrights and licenses remain in effect.**
