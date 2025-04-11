# Visual Studio Code - cheat

https://en.wikipedia.org/wiki/Visual_Studio_Code

## General

* Open the command palette: Strg+Shift+P
* Edit Settings: File > Preferences > Settings

## General Editing

### TODO: Setting: show line numbers in status bar

### Setting: Show whitespace characters

editor.renderWhitespace = All

### Setting: "Wrap (editor) tabs"

workbench.editor.wrapTabs = True

### Extension: "TODO highlight"

Highlights "TODO:" or "FIXME:" markers in the edited files and the editors scrollbar. Can be customized in ```settings.json```.

Id: wayou.vscode-todo-highlight

https://marketplace.visualstudio.com/items?itemName=wayou.vscode-todo-highlight

### Extension: "Trailing Spaces"

Highlights trailing spaces in the edited files with a red box while editing.

Id: shardulm94.trailing-spaces

https://marketplace.visualstudio.com/items/?itemName=shardulm94.trailing-spaces

### TODO: Extension: "Code Spell Checker"

Spell issues are underlined and highlighted in the editors scrollbar. Right click to get correction ideas or define exceptions.

Id: streetsidesoftware.code-spell-checker
https://marketplace.visualstudio.com/items?itemName=streetsidesoftware.code-spell-checker

TODO: different context menu entries
Exceptions are stored in settings.json of the workspace (TODO: or other options)

TODO: Is there a .something file to store the infos in a more general way (e.g. to be used by GitHub actions)?

---

## TODO: git

---

## TODO: Python

* pytest
* ...

### Extension: "Flake8" Linter

Python linter

* https://code.visualstudio.com/docs/python/linting
* https://marketplace.visualstudio.com/items?itemName=ms-python.flake8

TODO: .flake8 file

---

## TODO: C++

* gtest/gmock
* CMake
* C++
* ...

### Bugs: Strange Build Problems?

Delete the ```out``` folder of your workspace!

---

## TODO: Container

### TODO: Extension: "Docker"

Id: ms-azuretools.vscode-docker

### TODO: Extension: "Dev Containers"

* TODO: .devcontainer folder
* TODO: docker-compose handling

### Bugs: Reappearing "docker files changed" Message at Start?

Delete all containers!

