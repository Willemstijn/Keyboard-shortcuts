Favoriete Visual Studio Code shortcuts

- [Keyboard shortcuts](#keyboard-shortcuts)
  - [General](#general)
  - [Navigation](#navigation)
  - [MultiCursor and Selection](#multicursor-and-selection)
  - [Rich Language Editing](#rich-language-editing)
  - [Editor management](#editor-management)
  - [File management](#file-management)
  - [Display](#display)
  - [Debug](#debug)
  - [Integrated terminal](#integrated-terminal)
- [VS Code hacks](#vs-code-hacks)
  - [VS Code Keybinding to Toggle Focus Between and Editor and Terminal](#vs-code-keybinding-to-toggle-focus-between-and-editor-and-terminal)
  - [Markdown Table of contents](#markdown-table-of-contents)
- [VSC persoonlijke instellingen](#vsc-persoonlijke-instellingen)
  - [Exporting and importing specific settings](#exporting-and-importing-specific-settings)
  - [Windows](#windows)
  - [Linux](#linux)
- [Addons installed](#addons-installed)
  - [Getting a list of all installed extensions in VS Code](#getting-a-list-of-all-installed-extensions-in-vs-code)
  - [Addons list](#addons-list)
  - [A.k.a favoriete VS Code extensions](#aka-favoriete-vs-code-extensions)
- [Jupyter notebooks in VSC](#jupyter-notebooks-in-vsc)

# Keyboard shortcuts

## General
* ``Ctrl + Shift + P``  - Action panel
* ``Ctrl + K + M`` - Change/set file language
* ``Ctrl + B`` - Toggle side bar
* ``Ctrl + J`` - Toggle console panel
* ``Ctrl + Alt + N`` : Run 'Code runner' extension (for executing certain code in a consoles) 
* ``Ctrl + K - Ctrl + S`` - Show keyboard shortcut list in VSC
* ``Ctrl + K - Ctrl + R`` - Show keyboard shortcut list pdf
* ``Alt + L, Alt + O`` : Open html page with live server 
* ``Alt + L, Alt + C `` : Close live server

## Navigation
* ``Ctrl + ` `` - Open terminal screen (Toggle between editor and terminal after hack!)
* ``Ctrl + 1`` - Go to first editing pane (toggle between terminal and editor with these shortcuts!)
* ``Ctrl + 2`` - Go to second editing pane (etc.)

## MultiCursor and Selection
* ``Ctrl + SHIFT + ArrowUp/Down`` - Insert prompt vertical
* ``Ctrl + D`` - Add next occurrence
* ``Ctrl + SHIFT+L`` - Select all occurrences
* ``Alt + ArrowUp/Down`` - Move line up/down

## Rich Language Editing
* ``Ctrl + SHIFT + ArrowUp/Down`` - Copy current line above/below
* ``ALT +  SHIFT + Arrow up/down`` : Enter multiple prompts on lines on samen position for editing multiple lines at once
* ``Ctrl + Enter`` : Regel na invoeren
* ``Shift + Ctrl + Enter`` : Regel voor invoeren
* ``Alt + Shift + Arrow up down`` : Copy current line above/below
* ``Ctrl + x`` : Regel verwijderen 
* ``Ctrl + l`` : Regel selecteren 
* ``Ctrl + d`` : Woord en alle andere instanties van hetzelfde woord selecteren
* ``Ctrl + M`` : Naar haakje sluiten
* ``Ctrl + ]`` : Huidige regel inspringen
* ``Ctrl + [`` : Inspringen opheffen
* ``Ctrl + /`` : Commentaar regel maken (van selectie)
* ``Ctrl + Space`` : Property of methode selectie 

## Editor management
* ``Ctrl + Shift + P - Icons`` : installeer of gebruik geinstalleerde icon themes 
* ``Extensions openen + @`` : filteren en sorteren op catrgorieën etc. zoals @builtin voor reeds geinstalleerde extensions
* ``Ctrl + , `` : Instellingen openen (bijv. tabkleur actieve tab veranderen)
* ``Copy with syntax highlighting`` : uitgezet
* ``Minimap`` : disabled
* ``Extensions openen + screencast`` : toont bij opnemen van video de intedrukte toetsen
* ``@installed <modulenaam> `` : zoekt modulenaam op
* ``Ctrl + K, Ctrl + T `` : Change theme
* ``Alt + Shift + B`` : Open page with particular browser

## File management
* ``Ctrl + p`` : Bestand openen
* ``Ctrl + Shift + T`` : Opent recent gesloten bestanden
* ``Ctrl + r`` : Toont recent geopende folders en bestanden 
* ``code . `` : open vscode with current directory tree
* ``code . -r`` : open current vscode instance with current directory tree
* ``code -w filename.js`` : open file in code
* ``code -d file1.txt file2.txt`` : compare two files
* ``git config --global core.editor "code -w"`` : gebruik code als primaire git config editor
* ``git config --global -e`` : git config openen met code 

## Display
* ``Ctrl + Shift + e`` : Explorer balk
* ``Ctrl + Shift + f`` : Zoeken balk
* ``Ctrl + Shift + g`` : Source control (git) balk
* ``Ctrl + Shift + d`` : Debug balk
* ``Ctrl + Shift + x`` : Extensions balk
* ``Ctrl + Shift + V`` - Switch between Markdown Code and Markdown view
* ``Ctrl + K, V`` - Preview Code and markdown side by side
* ``Ctrl + k + z `` : Enter Zen mode (no distractions) 
* ``Ctrl + Shift + v`` : Voorbeeld tonen 

## Debug

## Integrated terminal
* ``Ctrl + PageDown/PageUp``  - Terminal scroll down / up
* ``Ctrl + Home / End``  - Scroll to bottom / top

https://shortcutworld.com/VSCode/win/Visual-Studio-Code_Shortcuts

# VS Code hacks

## VS Code Keybinding to Toggle Focus Between and Editor and Terminal

open your keybindings.json file Alt+k Alt+s (windows) Ctrl+k Ctrl+s (Linux), then you can add the following two entries to be able to toggle the focus between an editor and opened terminal (and have it remain open)

```
[
    {
        "key": "ctrl+`",
        "command": "workbench.action.terminal.focus",
        "when": "!terminalFocus"
    },
    {
        "key": "ctrl+`",
        "command": "workbench.action.focusActiveEditorGroup",
        "when": "terminalFocus"
    }
]
```

## Markdown Table of contents

Requires `Markdown All in One`

Install with:

```
Ctrl + P

ext install yzhang.markdown-all-in-one
```

Generate TOC with:

```
Ctrl + Shift + P

Select Markdown: Create Table of Contents
```

# VSC persoonlijke instellingen

## Exporting and importing specific settings

With the current version of Visual Studio Code as of this writing (1.22.1), you can find your settings in

Linux

	~/.config/Code/User

Windows 10

	C:\Users\username\AppData\Roaming\Code\User
	use these in Windows so you don't have to type the username in the path back and forth
	%APPDATA%\Code\User
	%USERPROFILE%\.vscode\extensions 
MacOS

	~/Library/Application Support/Code/User/

The files are settings.json and keybindings.json. Simply copy them to the target machine.


## Windows

Get the list of personal settings below by using the command: `Ctrl + ,`

```
{
    "editor.minimap.enabled": false,
    "editor.fontSize": 16,
    "editor.fontWeight": "500",
    "editor.fontFamily": "'Source Code Pro', Hack, Consolas, 'Courier New', monospace",
    "editor.formatOnSave": true,
    "editor.suggestSelection": "first",
    "workbench.sideBar.location": "right",
    "workbench.iconTheme": "material-icon-theme",
    "workbench.settings.editor": "json",
    "workbench.settings.openDefaultSettings": true,
    "workbench.statusBar.visible": true,
    // "python.pythonPath": "/usr/bin/python",
    // "python.pythonPath": "C:\\Users\\Bas\\AppData\\Local\\Programs\\Python\\Python38-32\\python.exe",
    "python.linting.enabled": true,
    "python.formatting.provider": "black",
    "python.languageServer": "Pylance",
    "debug.console.fontFamily": "default",
    "debug.console.fontSize": 16,
    "terminal.integrated.fontSize": 16,
    "terminal.integrated.fontWeight": "500",
    // "terminal.integrated.shell.windows": "C:\\Program Files\\Git\\bin\\bash.exe",
    "code-runner.executorMap": {
        "python": "$pythonPath -u $fullFileName"
    },
    "code-runner.clearPreviousOutput": true,
    "editor.quickSuggestionsDelay": 100,
    "zenMode.centerLayout": false,
    "zenMode.fullScreen": true,
    "zenMode.hideLineNumbers": false,
    "zenMode.hideTabs": false,
    "sync.gist": "31c1c7aa59f6aa27c9af94376123d1ad",
    "better-comments.multilineComments": true,
    "better-comments.highlightPlainText": false,
    "workbench.editorAssociations": {
        "*.ipynb": "jupyter.notebook.ipynb"
    },
    "python.defaultInterpreterPath": "C:\\Users\\BWN\\Anaconda3\\python.exe",
    "sync.autoDownload": true,
    "sync.autoUpload": true,
    "workbench.colorTheme": "Default Light+",
    "security.workspace.trust.untrustedFiles": "open",
    "window.zoomLevel": -1,
    "explorer.confirmDragAndDrop": false,
    "git.autofetch": true,
}
```

## Linux

```

```

# Addons installed

## Getting a list of all installed extensions in VS Code

1. Make sure you have the most current version of Visual Studio Code. If you install via a company portal, you might not have the most current version.

2. On machine A

Unix:

	code --list-extensions | xargs -L 1 echo code --install-extension

Windows (PowerShell, e. g. using Visual Studio Code's integrated Terminal):

	code --list-extensions | % { "code --install-extension $_" }

3. Copy and paste the echo output to machine B

Sample output

code --install-extension Angular.ng-template
code --install-extension DSKWRK.vscode-generate-getter-setter
code --install-extension EditorConfig.EditorConfig
code --install-extension HookyQR.beautify

==
Visual Studio Code looks for extensions under your extensions folder .vscode/extensions. Depending on your platform it is located:

Windows 
	%USERPROFILE%\.vscode\extensions
Mac 
	~/.vscode/extensions
Linux 
	~/.vscode/extensions

Alternately, just go to the Extensions, show installed extensions, and install those on your target installation. For me, copying the extensions worked just fine, but it may be extension-specific, particularly if moving between platforms, depending on what the extension does.

## Addons list

```
[
  {
    "metadata": {
      "id": "88eb8072-5ab1-457b-9835-6d92196388a3",
      "publisherId": "almenon.arepl",
      "publisherDisplayName": "almenon"
    },
    "name": "arepl",
    "publisher": "almenon",
    "version": "2.0.1"
  },
  {
    "metadata": {
      "id": "2d6fea35-f68e-461d-9b7b-5cd05be99451",
      "publisherId": "njpwerner.autodocstring",
      "publisherDisplayName": "njpwerner"
    },
    "name": "autodocstring",
    "publisher": "njpwerner",
    "version": "0.5.4"
  },
  {
    "metadata": {
      "id": "5178733e-4b02-4829-95c5-1ce970847c23",
      "publisherId": "teabyii.ayu",
      "publisherDisplayName": "teabyii"
    },
    "name": "ayu",
    "publisher": "teabyii",
    "version": "0.20.1"
  },
  {
    "metadata": {
      "id": "7a0110bb-231a-4598-aa1b-0769ea46d28b",
      "publisherId": "aaron-bond.better-comments",
      "publisherDisplayName": "aaron-bond"
    },
    "name": "better-comments",
    "publisher": "aaron-bond",
    "version": "2.1.0"
  },
  {
    "metadata": {
      "id": "f583eafd-aa0d-4ccb-8f44-d1e610389660",
      "publisherId": "CoenraadS.bracket-pair-colorizer",
      "publisherDisplayName": "CoenraadS"
    },
    "name": "bracket-pair-colorizer",
    "publisher": "CoenraadS",
    "version": "1.0.61"
  },
  {
    "metadata": {
      "id": "a6a0c5b2-d078-4bf5-a9ee-4e37054414b3",
      "publisherId": "formulahendry.code-runner",
      "publisherDisplayName": "formulahendry"
    },
    "name": "code-runner",
    "publisher": "formulahendry",
    "version": "0.11.2"
  },
  {
    "metadata": {
      "id": "e337c67b-55c2-4fef-8949-eb260e7fb7fd",
      "publisherId": "Shan.code-settings-sync",
      "publisherDisplayName": "Shan"
    },
    "name": "code-settings-sync",
    "publisher": "Shan",
    "version": "3.4.3"
  },
  {
    "metadata": {
      "id": "fb1a0ad6-6285-4b5e-b07d-826dee8e2a85",
      "publisherId": "ankitcode.firefly",
      "publisherDisplayName": "ankitcode"
    },
    "name": "firefly",
    "publisher": "ankitcode",
    "version": "3.0.1"
  },
  {
    "metadata": {
      "id": "1efd3211-484a-47d0-ae12-f9eb4245a6a7",
      "publisherId": "ms-python.gather",
      "publisherDisplayName": "ms-python"
    },
    "name": "gather",
    "publisher": "ms-python",
    "version": "2021.1.0"
  },
  {
    "metadata": {
      "id": "4de763bd-505d-4978-9575-2b7696ecf94e",
      "publisherId": "eamodio.gitlens",
      "publisherDisplayName": "eamodio"
    },
    "name": "gitlens",
    "publisher": "eamodio",
    "version": "11.2.1"
  },
  {
    "metadata": {
      "id": "eaa2127d-cb69-4ab9-8505-a60c9ee5f28b",
      "publisherId": "oderwat.indent-rainbow",
      "publisherDisplayName": "oderwat"
    },
    "name": "indent-rainbow",
    "publisher": "oderwat",
    "version": "7.5.0"
  },
  {
    "metadata": {
      "id": "6c2f1801-1e7f-45b2-9b5c-7782f1e076e8",
      "publisherId": "ms-toolsai.jupyter",
      "publisherDisplayName": "ms-toolsai"
    },
    "name": "jupyter",
    "publisher": "ms-toolsai",
    "version": "2020.12.414227025"
  },
  {
    "metadata": {
      "id": "98790d67-10fa-497c-9113-f6c7489207b2",
      "publisherId": "yzhang.markdown-all-in-one",
      "publisherDisplayName": "yzhang"
    },
    "name": "markdown-all-in-one",
    "publisher": "yzhang",
    "version": "3.4.0"
  },
  {
    "metadata": {
      "id": "5db78037-f674-459f-a236-db622c427c5b",
      "publisherId": "PKief.material-icon-theme",
      "publisherDisplayName": "PKief"
    },
    "name": "material-icon-theme",
    "publisher": "PKief",
    "version": "4.5.0"
  },
  {
    "metadata": {
      "id": "26a529c9-2654-4b95-a63f-02f6a52429e6",
      "publisherId": "zhuangtongfa.material-theme",
      "publisherDisplayName": "zhuangtongfa"
    },
    "name": "material-theme",
    "publisher": "zhuangtongfa",
    "version": "3.9.13"
  },
  {
    "metadata": {
      "id": "de040f22-8a86-45da-9cfe-d4f4c0c8fdc0",
      "publisherId": "obrejla.netbeans-light-theme",
      "publisherDisplayName": "obrejla"
    },
    "name": "netbeans-light-theme",
    "publisher": "obrejla",
    "version": "2.0.2"
  },
  {
    "metadata": {
      "id": "fef63133-dae3-40fb-b81d-6da7617b4b1e",
      "publisherId": "techer.open-in-browser",
      "publisherDisplayName": "techer"
    },
    "name": "open-in-browser",
    "publisher": "techer",
    "version": "2.0.0"
  },
  {
    "metadata": {
      "id": "3890a034-fd6e-41f7-a689-4bfb8c250edd",
      "publisherId": "ex-codes.pine-script-syntax-highlighter",
      "publisherDisplayName": "ex-codes"
    },
    "name": "pine-script-syntax-highlighter",
    "publisher": "ex-codes",
    "version": "1.0.1"
  },
  {
    "metadata": {
      "id": "4b81241f-f3d1-4520-8611-0ba585f3d322",
      "publisherId": "NikosKornarakis.predawn-twilight",
      "publisherDisplayName": "NikosKornarakis"
    },
    "name": "predawn-twilight",
    "publisher": "NikosKornarakis",
    "version": "1.0.0"
  },
  {
    "metadata": {
      "id": "f1f59ae4-9318-4f3c-a9b5-81b2eaa5f8a5",
      "publisherId": "ms-python.python",
      "publisherDisplayName": "ms-python"
    },
    "name": "python",
    "publisher": "ms-python",
    "version": "2021.1.502429796"
  },
  {
    "metadata": {
      "id": "3792588c-3d35-442d-91ea-fe6a755e8155",
      "publisherId": "mechatroner.rainbow-csv",
      "publisherDisplayName": "mechatroner"
    },
    "name": "rainbow-csv",
    "publisher": "mechatroner",
    "version": "1.8.1"
  },
  {
    "metadata": {
      "id": "607fd052-be03-4363-b657-2bd62b83d28a",
      "publisherId": "ms-vscode-remote.remote-ssh",
      "publisherDisplayName": "ms-vscode-remote"
    },
    "name": "remote-ssh",
    "publisher": "ms-vscode-remote",
    "version": "0.63.0"
  },
  {
    "metadata": {
      "id": "bfeaf631-bcff-4908-93ed-fda4ef9a0c5c",
      "publisherId": "ms-vscode-remote.remote-ssh-edit",
      "publisherDisplayName": "ms-vscode-remote"
    },
    "name": "remote-ssh-edit",
    "publisher": "ms-vscode-remote",
    "version": "0.63.0"
  },
  {
    "metadata": {
      "id": "f0c5397b-d357-4197-99f0-cb4202f22818",
      "publisherId": "ms-vscode-remote.remote-wsl",
      "publisherDisplayName": "ms-vscode-remote"
    },
    "name": "remote-wsl",
    "publisher": "ms-vscode-remote",
    "version": "0.52.0"
  },
  {
    "metadata": {
      "id": "dda49fd5-1f3b-4d25-bf61-4fc41905ede5",
      "publisherId": "humao.rest-client",
      "publisherDisplayName": "humao"
    },
    "name": "rest-client",
    "publisher": "humao",
    "version": "0.24.4"
  },
  {
    "metadata": {
      "id": "6a2bbab0-d8f0-43fa-9b26-e6a3b7892a0b",
      "publisherId": "mtxr.sqltools",
      "publisherDisplayName": "mtxr"
    },
    "name": "sqltools",
    "publisher": "mtxr",
    "version": "0.23.0"
  },
  {
    "metadata": {
      "id": "34647879-c168-49c3-8cb4-f7705064ca32",
      "publisherId": "ms-vscode.Theme-PredawnKit",
      "publisherDisplayName": "ms-vscode"
    },
    "name": "Theme-PredawnKit",
    "publisher": "ms-vscode",
    "version": "0.1.4"
  },
  {
    "metadata": {
      "id": "daf8b44d-8aae-4da2-80c5-1f770219f643",
      "publisherId": "DavidAnson.vscode-markdownlint",
      "publisherDisplayName": "DavidAnson"
    },
    "name": "vscode-markdownlint",
    "publisher": "DavidAnson",
    "version": "0.38.0"
  },
  {
    "metadata": {
      "id": "eaee103c-e866-4b73-87f8-3749cab64da2",
      "publisherId": "alexcvzz.vscode-sqlite",
      "publisherDisplayName": "alexcvzz"
    },
    "name": "vscode-sqlite",
    "publisher": "alexcvzz",
    "version": "0.11.1"
  },
  {
    "metadata": {
      "id": "ff96f1b4-a4b8-45ef-8ecf-c232c0cb75c8",
      "publisherId": "hbenl.vscode-test-explorer",
      "publisherDisplayName": "hbenl"
    },
    "name": "vscode-test-explorer",
    "publisher": "hbenl",
    "version": "2.19.5"
  },
  {
    "metadata": {
      "id": "876e8f93-74d0-4f4f-91b7-34a09f19f444",
      "publisherId": "VisualStudioExptTeam.vscodeintellicode",
      "publisherDisplayName": "VisualStudioExptTeam"
    },
    "name": "vscodeintellicode",
    "publisher": "VisualStudioExptTeam",
    "version": "1.2.11"
  }
]
```

Zie ook: https://gist.github.com/Willemstijn/31c1c7aa59f6aa27c9af94376123d1ad


## A.k.a favoriete VS Code extensions

Installed VS Code extensions (@installed)

* Azure account
* Azure functions
* Beautify
* Debugger for Chrome
* Debugger for Firefox
* Django
* Docker
* Excel to markdown table
* HTML Boilerplate
* Live server
* MagicPython
* Markdown All in One
* Markdown code block
* markdown PDF
* Markdown table prettifier
* MarkdownLint
* Open in Browser
* Pine script syntax highlighting
* PowerShell
* Python
* Python extended
* Python extension pack
* REG (registry script language)
* Remote - WSL (alleen Linux in Windows)
* TSlint
* Visual studio intellicode
* Vscode icons
* Vscode-pdf


# Jupyter notebooks in VSC

Van https://www.youtube.com/watch?v=FSdIoJdSnig

* Installeer VSC (duh)
* Installeer Python
* Installeer Anaconda (heeft niet mijn voorkeur - Ik gebruik Linux) (https://linuxhandbook.com/anaconda-linux/)

* Ctrl+Shift+P
* Zoek "create new blank Jupyter notebook"


Keyboard shortcuts

Zie ook: 

* < https://code.visualstudio.com/docs/python/python-tutorial/?&WT.mc_id=vstoolbox-c9-niner
* https://code.visualstudio.com/docs/python/jupyter-support
* https://marketplace.visualstudio.com/items?itemName=ms-python.python


