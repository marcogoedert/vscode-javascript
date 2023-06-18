# vscode-javascript

## JavaScript ES6 code snippets (Updated)

---

[![The MIT License](https://img.shields.io/badge/license-MIT-orange.svg?style=flat-square)](http://opensource.org/licenses/MIT)
![Visual Studio Marketplace Version](https://img.shields.io/visual-studio-marketplace/v/MarcoGoedert.JavaScriptSnippetsUpdated.svg?style=flat-square)
![Visual Studio Marketplace Installs](https://img.shields.io/visual-studio-marketplace/i/MarcoGoedert.JavaScriptSnippetsUpdated.svg?style=flat-square)
![Visual Studio Marketplace Rating](https://img.shields.io/visual-studio-marketplace/r/MarcoGoedert.JavaScriptSnippetsUpdated.svg?style=flat-square)

This extension contains code snippets for JavaScript in ES6 syntax for [Vs Code][code] editor (supports both JavaScript and TypeScript). **It includes snippets for new features released with ECMAScript 2023.**

> This extension is a fork from the original [JavaScript (ES6) code snippets](https://marketplace.visualstudio.com/items?itemName=xabikos.JavaScriptSnippets) made by [xabikos](https://github.com/xabikos). The original extension is no longer maintained and the author is not accepting pull requests. This fork is maintained by [Marco Goedert](https://github.com/marcogoedert).

## Contributors

- [Marco Goedert](https://github.com/marcogoedert)
- [Aloísio Bastian](https://github.com/Aloisio-Miguel)
- [Fernando Elger](https://github.com/fernandoelger)

### Note

**All the snippets include the final semicolon `;` There is a fork of those snippets [here](https://marketplace.visualstudio.com/items?itemName=jmsv.JavaScriptSnippetsStandard)
made by @jmsv where semicolons are not included. So feel free to use them according to your needs.**

## Installation

In order to install an extension you need to launch the Command Palette (Ctrl + Shift + P or Cmd + Shift + P) and type Extensions.
There you have either the option to show the already installed snippets or install new ones. Search for _JavaScript (ES6) code snippets_ and install it.

## Supported languages (file extensions)

- JavaScript (.js)
- TypeScript (.ts)
- JavaScript React (.jsx)
- TypeScript React (.tsx)
- Html (.html)
- Vue (.vue)

## Snippets

Below is a list of all available snippets and the triggers of each one. The **⇥** means the `TAB` key.

### ECMAScript 2023 new features

|    Trigger | Content                                                                                                                  |
| ---------: | ------------------------------------------------------------------------------------------------------------------------ |
|     `trv→` | Returns a new array with reversed elements `${1:array}.toReversed();`                                                    |
|     `tsd→` | Returns a new array with sorted elements `${1:array}.toSorted(${2:compareFn});`                                          |
|     `tsp→` | Returns a new array with spliced elements `${1:array}.toSpliced(${2:start}, ${3:deleteCount}, ...${4:items});`           |
|     `with` | Returns a new array with a changed value at the specified index `${1:array}.with(${2:index}, ${3:value});`               |
|    `tatrv` | Returns a new TypedArray with reversed elements `${1:typedArray}.toReversed();`                                          |
|    `tatsd` | Returns a new TypedArray with sorted elements `${1:typedArray}.toSorted(${2:compareFn});`                                |
|   `tawith` | Returns a new TypedArray with a changed value at the specified index `${1:typedArray}.with(${2:index}, ${3:value});`     |
|       `fl` | Finds the last element in the array that satisfies the condition `array.findLast(${1:condition});`                       |
|      `fli` | Finds the index of the last element in the array that satisfies the condition `array.findLastIndex(${1:condition});`     |
| `hashbang` | Hashbang Grammar `#!/usr/bin/env node\n'use strict';\nconsole.log(1);\n#!/usr/bin/env node\nexport {};\nconsole.log(1);` |
|      `sym` | Creates a unique Symbol key `const ${1:key} = Symbol('${2:description}');$0`                                             |
|      `wms` | Sets a value in a WeakMap using a Symbol key `${1:weakMap}.set(${2:key}, ${3:value});$0`                                 |
|      `wmg` | Gets a value from a WeakMap using a Symbol key `${1:weakMap}.get(${2:key});$0`                                           |
|      `wmh` | Checks if a WeakMap has a value associated with a Symbol key `${1:weakMap}.has(${2:key});$0`                             |
|      `ols` | Sets a value in an object lookup using a Symbol key `${1:objectLookup}.set(${2:symbol}, ${3:object});$0`                 |
|      `olg` | Gets a value from an object lookup using a Symbol key `${1:objectLookup}.get(${2:symbol});$0`                            |
|      `rfr` | Creates a reference in a RefBookkeeper using a Symbol key `${1:refs}.ref(${2:object});$0`                                |
|      `rfd` | Gets the object associated with a Symbol key in a RefBookkeeper `${1:refs}.deref(${2:symbol});$0`                        |

References:

- [tc39/proposal-array-find-from-last](https://github.com/tc39/proposal-array-find-from-last): Proposal for `.findLast()` and `.findLastIndex()` methods on array and typed array.
- [tc39/proposal-change-array-by-copy](https://github.com/tc39/proposal-change-array-by-copy): Provides additional methods on `Array.prototype` and `TypedArray.prototype` to enable changes on the array by returning a new copy of it with the change.
- [tc39/proposal-symbols-as-weakmap-keys](https://github.com/tc39/proposal-symbols-as-weakmap-keys): This proposal extends the WeakMap API to allow usage of unique Symbols as keys.
- [tc39/proposal-hashbang](https://github.com/tc39/proposal-hashbang): This proposal is to match de-facto usage in some CLI JS hosts that allow for Shebangs / Hashbang. Such hosts strip the hashbang in order to generate valid JS source texts before passing to JS engines currently. This would move the stripping to engines, it does unify and standardize how that is done.

### Import and export

| Trigger | Content                                                                                                |
| ------: | ------------------------------------------------------------------------------------------------------ |
|  `imp→` | imports entire module `import fs from 'fs';`                                                           |
|  `imn→` | imports entire module without module name `import 'animate.css'`                                       |
|  `imd→` | imports only a portion of the module using destructing `import {rename} from 'fs';`                    |
|  `ime→` | imports everything as alias from the module `import * as localAlias from 'fs';`                        |
|  `ima→` | imports only a portion of the module as alias `import { rename  as localRename } from 'fs';`           |
|  `rqr→` | require package `require('');`                                                                         |
|  `req→` | require package to const `const packageName = require('packageName');`                                 |
|  `mde→` | default module.exports `module.exports = {};`                                                          |
|  `env→` | exports name variable `export const nameVariable = localVariable;`                                     |
|  `enf→` | exports name function `export const log = (parameter) => { console.log(parameter);};`                  |
|  `edf→` | exports default function `export default function fileName (parameter){ console.log(parameter);};`     |
|  `ecl→` | exports default class `export default class Calculator { };`                                           |
|  `ece→` | exports default class by extending a base one `export default class Calculator extends BaseClass { };` |

### Class helpers

| Trigger | Content                                                        |
| ------: | -------------------------------------------------------------- |
|  `con→` | adds default constructor in the class `constructor() {}`       |
|  `met→` | creates a method inside a class `add() {}`                     |
|  `pge→` | creates a getter property `get propertyName() {return value;}` |
|  `pse→` | creates a setter property `set propertyName(value) {}`         |

### Various methods

|  Trigger | Content                                                                                                       |
| -------: | ------------------------------------------------------------------------------------------------------------- |
|   `fre→` | forEach loop in ES6 syntax `array.forEach(currentItem => {})`                                                 |
|   `fof→` | for ... of loop `for(const item of object) {}`                                                                |
|   `fin→` | for ... in loop `for(const item in object) {}`                                                                |
|  `anfn→` | creates an anonymous function `(params) => {}`                                                                |
|   `nfn→` | creates a named function `const add = (params) => {}`                                                         |
|   `dob→` | destructing object syntax `const {rename} = fs`                                                               |
|   `dar→` | destructing array syntax `const [first, second] = [1,2]`                                                      |
|   `sti→` | set interval helper method `setInterval(() => {});`                                                           |
|   `sto→` | set timeout helper method `setTimeout(() => {});`                                                             |
|  `prom→` | creates a new Promise `return new Promise((resolve, reject) => {});`                                          |
| `thenc→` | adds then and catch declaration to a promise `.then((res) => {}).catch((err) => {});`                         |
|   `trv→` | returns a new array with the elements in reversed order `const reversedArray = ${1:array}.toReversed();`      |
|   `tsd→` | returns a new array with the elements sorted `const ${1:sortedArray} = ${2:array}.toSorted();`                |
|   `tsp→` | returns a new array with the elements spliced `const ${1:splicedArrray} = ${2:array}.toSpliced(${3:values});` |

### Console methods

| Trigger | Content                                                            |
| ------: | ------------------------------------------------------------------ |
|  `cas→` | console alert method `console.assert(expression, object)`          |
|  `ccl→` | console clear `console.clear()`                                    |
|  `cco→` | console count `console.count(label)`                               |
|  `cdb→` | console debug `console.debug(object)`                              |
|  `cdi→` | console dir `console.dir`                                          |
|  `cer→` | console error `console.error(object)`                              |
|  `cgr→` | console group `console.group(label)`                               |
|  `cge→` | console groupEnd `console.groupEnd()`                              |
|  `clg→` | console log `console.log(object)`                                  |
|  `clo→` | console log object with name `console.log('object :>> ', object);` |
|  `ctr→` | console trace `console.trace(object)`                              |
|  `cwa→` | console warn `console.warn`                                        |
|  `cin→` | console info `console.info`                                        |
|  `clt→` | console table `console.table`                                      |
|  `cti→` | console time `console.time`                                        |
|  `cte→` | console timeEnd `console.timeEnd`                                  |

[code]: https://code.visualstudio.com/
