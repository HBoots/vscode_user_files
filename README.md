# VSCode Configuration

This repository comes directly from the configuration files on the home machine.

`~/.config/Code/User`

It includes keybindings, editor settings and snippets files. All other directories are ignored.

#### Path to keybindings & editor settings files ...

`~/.config/Code/User`

`keybindings.json` overrides defaults.

`settings.json` is the complete settings file and includes both defaults and custom settings.

#### Path to snippet files ...

`~/.config/Code/User/snippets`

## Some Notes on a Few Settings

Enter a newline without accepting intellisense suggestion.  
`"editor.acceptSuggestionOnEnter" : "off"`

Control whether a closing paren overtypes an adjacent closing paren.  
`"editor.autoClosingOvertype": "never"`

Control whether brackets / parens will auto close when adjacent to another character.  
`"editor.autoClosingBrackets": "always"`

Control whether a folder with a single file will display on a single line in explorer.  
`"explorer.compactFolders": false`

Control whether autocomplete still functions after using a code snippet.
`"editor.suggest.snippetsPreventQuickSuggestions": false"`

Disable css linting rules in `settings.json`.
`"css.lint.emptyRules": "ignore"`

## Snippet Syntax

Each snippet is defined under a snippet name and has a prefix, body and description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. The same prefix trigger can be used for multiple snippets. The Intellisence pop up window will list all snippets by snippet name that are associated with the given prefix.

Placeholders (`$1`) with the same ids will yeild multiple simultaneous cursor positions.

Note that the body of a snippet is an array where each element is a single line and line break. Any prefered indentation will have to be explicitly entered with tab characters (`\t`). Although this may be unecessary if relying on auto formating.

_Example:_

```
"Print to console": {
	"prefix": "log",
	"body": [
		"console.log('$1');",
		"$2"
	],
	"description": "Log output to console"
}
```

Global and project level snippet files are supported as well.

## Extensions

VSCode extensions are stored in ...  
`~/.vscode/extensions`

A list of currently installed extensions can be accessed in the command line with...  
`$ code --list-extensions`

There are some 3rd party tools that will help migrate extensions between VSCode installations.

Extensions installed as of 7/27/24:

batisteo.vscode-django
dbaeumer.vscode-eslint
digitalbrainstem.javascript-ejs-support
esbenp.prettier-vscode
hediet.vscode-drawio
humao.rest-client
kubescape.kubescape
mongodb.mongodb-vscode
ms-azuretools.vscode-docker
ms-kubernetes-tools.vscode-kubernetes-tools
ms-python.debugpy
ms-python.isort
ms-python.python
ms-vscode-remote.remote-containers
ms-vscode-remote.remote-ssh
ms-vscode-remote.remote-ssh-edit
ms-vscode-remote.remote-wsl
ms-vscode-remote.vscode-remote-extensionpack
ms-vscode.remote-explorer
ms-vscode.remote-server
redhat.java
redhat.vscode-yaml
ritwickdey.liveserver
visualstudioexptteam.intellicode-api-usage-examples
visualstudioexptteam.vscodeintellicode
vscjava.vscode-java-debug
vscjava.vscode-java-dependency
vscjava.vscode-java-pack
vscjava.vscode-java-test
vscjava.vscode-maven
