[![](https://vsmarketplacebadge.apphb.com/version/bierner.dart-inline-html.svg)](https://marketplace.visualstudio.com/items?itemName=bierner.dart-inline-html) [![Build Status](https://travis-ci.org/mjbvz/vscode-dart-inline-html.svg?branch=master)](https://travis-ci.org/mjbvz/vscode-dart-inline-html)

Adds syntax highlighting and language support for html inside of JavaScript and TypeScript tagged template strings, such as used in [dart-inline-html](https://github.com/PolymerLabs/dart-inline-html) and other frameworks.

![](https://github.com/mjbvz/vscode-dart-inline-html/raw/master/docs/example.gif)


## Features

- Syntax highlighting of inline html blocks.
- IntelliSense for html tags and attributes.
- Quick info hovers on tags.
- Formatting support.
- Auto closing tags.
- Folding html.
- CSS completions in style blocks.
- Works with literal html strings that contain placeholders.

## Usage
The dart-inline-html extension adds highlighting and IntelliSense for dart-inline-html template strings in JavaScript and TypeScript. It works out of the box when you use VS Code's built-in version of TypeScript.

If you are using VS Code 1.30 or older and are [using a workspace version of typescript](https://code.visualstudio.com/Docs/languages/typescript#_using-newer-typescript-versions), you must currently configure the TS Server plugin manually by following [these instructions](https://github.com/Microsoft/typescript-dart-inline-html-plugin#usage)

## Configuration

You can either configure this plugin using a `tsconfig` or `jsconfig` as described [here](https://github.com/Microsoft/typescript-dart-inline-html-plugin#configuration), or configure the plugin using VS Code. This requires VS Code 1.30+ and TS 3.2+. Note the VS Code based configuration override the `tsconfig` or `jsconfig` configuration.

### Tags
This extension adds html IntelliSense to any template literal [tagged](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Template_literals) with `html` or `raw`:

```js
import {html} from 'dart-inline-html'

const a = html`
    <div></div>
`
```

You can enable IntelliSense for other tag names by settings `"dart-inline-html.tags"`:

```json
"dart-inline-html.tags": [
    "html",
    "template"
]
```

### Formatting
The plugin formats html code by default. You can disable this by setting `"dart-inline-html.format.enabled": false`:

```json
"dart-inline-html.format.enabled": false
```
