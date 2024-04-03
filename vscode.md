# vs code notes

## how to make snippets
%
Open Command box and search for Configure snippets  
Select the language for which you want to make a snippet  
Follow the example

This is an example for surround an selection with quotes in markdown
```json

		"surround as code block": {
			"prefix": "code",
			"body": [
				"```${1:language}",
				"${TM_SELECTED_TEXT}",
				"```${0}"
			],
			"description": "Surround as code block"
		},
```

## how to surround text in an snippet
%
use placeholder ${TM_SELECTED_TEXT}

```json
"body": [
    "before",
    "${TM_SELECTED_TEXT}",
    "after"
]

```
## How to use placeholders in VS Code snippets
How to provide custom fields in your snippets.
%
You can add variables to your snippet by provide numbered locaitons to your snippets.

F.e.  "${1:field1} is field 1"

**Attention {0} is the final position of the snippet**

## How to make multiple choices for keywords in snippets
%
You can add a list of keywords to a tab location by providing the following

```fsharp
"${1|choice1,Choice2|}"
```
*Attention: Note the '|' at the end of the list!*
## How to bind to a specific snippet
How to add a custom keybinding to your favorite snippets?
%
You can an entry into the keybindings.json with the following data:

```fsharp
{
	"key": "Ctrl+Alt+Shift+&",
	"command" : "editor.action.insertSnippet",
	"when": "editorTextFocus",
	"args":{
		"name":"mySnippetName"
	}
}
```