# mdEditor

> **Awesome Markdown Editor/Workspace for VS Code**
>
> **v2.0.0**

## Table of Contents

- [About](#about)
- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [References](#references)

<a href="https://github.com/killshot13/mdEditor"><img align="right" width="605" height="395" src="https://github.com/killshot13/mdEditor/blob/main/images/markdown-to-html.jpg" alt="HTML file created with mdEditor"></a>
<p align="center">
<a href="https://github.com/killshot13/mdEditor"><img width="605" height="395" src="https://github.com/killshot13/mdEditor/blob/main/images/markdown-to-docx.jpg" alt="DOCX file created with mdEditor"></a>
</p>

## About <a name = "about"></a>

### Features

- Auto-checks for errors/problems and generates a detailed output for any broken rules.

- Lints and runs auto-fix on save which will correct/reformat most common errors.

- Supports the creation of `.pdf`, `.docx`, and `.html` files, which can be exported and viewed with MS Word, Adobe Acrobat, or the browser.

- Enforces syntax for any markdown flavor with a simple on/off option for every rule.

- All `html` files are linked to a basic stylesheet during creation so they look natural if viewed with the browser.

### Details

mdEditor provides the configuration guidelines and creates the structure for an awesome VSCode Markdown editor. By creating a reusable `code-workspace`, the main portion of your IDE environment is protected from rule conflicts.

Unless you work with Markdown on a daily basis, the editor is designed to be installed locally at the user level. Markdown files can be created in the editor workspace, and existing files imported as needed for easy linting.

mdEditor is an adaptation derived from the brainchild of [Dave Johnson](https://twitter.com/thisDaveJ), which he detailed a couple years ago in [an article](https://thisdavej.com/build-an-amazing-markdown-editor-using-visual-studio-code-and-pandoc/) on his blog.

---

<p align="center">
    <a href="https://github.com/killshot13/mdEditor"><img width="780" height="520" src="https://github.com/killshot13/mdEditor/blob/main/images/mdEditor.gif" alt="GIF file showing how mdEditor works"></a>
</p>

## Prerequisites <a name = "prerequisites"></a>

**[Visual Studio Code](https://code.visualstudio.com/Download)**
This should be self-explanatory.

**[Pandoc](http://pandoc.org/installing.html)**
This may require some guidance if you don't currently use Pandoc. I wrote a gist to help first-time users; here is [the link](https://gist.github.com/killshot13/5b379355d275e79a5cb1f03c841c7d53).

### Installation <a name = "installation"></a>

Decide where the core mdEditor files should live on your local drive (reference [About](#about) for more), then clone [mdEditor](https://github.com/killshot13/mdEditor.git) to that location.

Now, open mdEditor at the base directory using VSCode. Your IDE will auto-discover the `.code-workspace` file and prompt you to reopen the folder as a workspace. Confirm this choice, unless you wish to use a different configuration.

If so, there is a blank `settings.json` in the `.vscode` folder for you. Otherwise, you should disregard said folder completely.

We still need to pass the linting rules and Pandoc style guide to the editor workspace.

You should have noticed a prompt once you entered the workspace about installing the recommended extensions. If you have not done so already, go ahead and approve the install.

If for some reason you did not receive a prompt or have already closed the notification tab, not to worry. Just install these VSCode extensions, leaving the settings at their default values.

--> [markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint)

--> [vscode-pandoc](https://marketplace.visualstudio.com/items?itemName=ChrisChinchilla.vscode-pandoc)

### Tree View

Now, using this diagram, verify the file structure of your local mdEditor is free from any discrepancies.

##### _mdEditor/_

 - [.github](./.github)
   - [ISSUE_TEMPLATE](./.github/ISSUE_TEMPLATE)
	 	- [bug_report.md](./.github/ISSUE_TEMPLATE/bug_report.md)
		- [custom.md](./.github/ISSUE_TEMPLATE/custom.md)
		- [feature_request.md](./.github/ISSUE_TEMPLATE/feature_request.md)
	- [CONTRIBUTING.md](./.github/CONTRIBUTING.md)
	- [ISSUE_TEMPLATE.md](./.github/ISSUE_TEMPLATE.md)
	- [PULL_REQUEST_TEMPLATE.md](./.github/PULL_REQUEST_TEMPLATE.md)
 - [.vscode](./.vscode)
	 - [extensions.json](./.vscode/extensions.json)
	 - [settings.json](./.vscode/settings.json)
 - [images](./images)
   - [markdown-to-docx.jpg](./images/markdown-to-docx.jpg)
   - [markdown-to-html.jpg](./images/markdown-to-html.jpg)
   - [markdown-to-pdf.jpg](./images/markdown-to-pdf.jpg)
   - [mdEditor.gif](./images/mdEditor.gif)
 - [CHANGELOG.md](./CHANGELOG.md)
 - [LICENSE](./LICENSE)
 - [md](./md)
   - [test.txt](./md/test.txt)
 - [mdEditor.code-workspace](./mdEditor.code-workspace)
 - [styles](./styles)
   - [style.css](./styles/style.css)
   - [rules.md](./styles/rules.md)
 - [README.md](./README.md)

If the file structure matches, installation is complete. Well done!

> **NOTE: If using Linux you must uncomment the `pandoc.htmlOptString` in the `mdEditor.code-workspace` file. The current version, which uses Windows OS file separators, must be replaced with the Linux version; otherwise, the css styles will not be applied correctly.**

## Usage <a name = "usage"></a>

To test linting & formatting, click the `test.txt` file (in the `md` folder); it should open in the main editor window.

In the sidebar, keeping the `test.txt` tab in focus, change the filetype from `txt` to `md` and save.

Check the output in the PROBLEMS tab of your lower (terminal) panel. Several formatting violations should appear. Now make a tiny edit and save again. Most of the errors should be gone, having been corrected automatically.

To test the filetype output, enter the key combination `CTRL + K`, then press `P`. Options to create `.pdf`, `.docx`, or `.html` file should appear in the dropdown. Click each option in turn and confirm the desired result was produced.

Workspace setup is now complete and mdEditor is ready to use.

>NOTE: The `syntax.md` file in the `styles` folder contains a detailed description of the linting rules available within the editor workspace. Most linting rules can be simply toggled on/off by editing the `.markdownlint.json` file using this syntax.

```json
{
	"MD-XXX": Boolean
}
```

Happy markdown'ing! :)

[mdEditor](https://github.com/killshot13/mdEditor) is free software released under the [MIT license](https://github.com/killshot13/mdEditor/blob/main/LICENSE). Copyright 2020-2021 Michael Rehnert

## References <a name = "references"></a>

_Extensive credit is owed to [Dave Johnson](https://twitter.com/thisDaveJ) for inspiring me to create mdEditor after reading [this guide](https://thisdavej.com/build-an-amazing-markdown-editor-using-visual-studio-code-and-pandoc) he authored._

_Additional credit and appreciation is extended to the creators, contributors, and maintainers of the following open-source software projects._

[markdownlint](https://marketplace.visualstudio.com/items?itemName=DavidAnson.vscode-markdownlint) is free software released under the [MIT license](https://marketplace.visualstudio.com/items/DavidAnson.vscode-markdownlint/license). Copyright (c) David Anson

[vscode-pandoc](https://marketplace.visualstudio.com/items?itemName=ChrisChinchilla.vscode-pandoc) is free software released under the [MIT license](https://marketplace.visualstudio.com/items/ChrisChinchilla.vscode-pandoc/license). Copyright (c) 2023 Chris Ward / aka Chris Chinchilla

[Pandoc](https://pandoc.org) is free software released under the [GPL](https://www.gnu.org/licenses/gpl-3.0.html). Copyright 2006–2022 [John MacFarlane](https://johnmacfarlane.net).

[VS Code](https://code.visualstudio.com/) is free software released under the [MIT license](https://github.com/microsoft/vscode/blob/main/LICENSE.txt). The project's [source code](https://github.com/microsoft/vscode) is available on GitHub. Copyright (c) 2015 - present [Microsoft Corporation](https://www.microsoft.com)

All software programs, extensions, plugins, and digital content referenced and/or used in the documentation and/or installation guide of mdEditor is the respective intellectual property of the creators, developers, and owners thereof and is entitled to the protections granted under U.S. Copyright law.
