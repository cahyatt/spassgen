# spassgen
A versatile, safe, and customizable password generator.

## Installation

##### NPM
```bash
$ npm i spassgen
```

## Features
* Generates safe passwords
* Doesn't save any passwords generated
* Customizable password generation and output
* Easy to use!

## Usage
To initialize **spassgen**, simply require it!
```js
const _generate = require("spassgen");
```

Every time you generate a password, whether it has its default settings or you customize the generation, you will use this function to generate the password:
```js
_generate();
```

To get a different data type output for the password, include a table in the parentheses:
```js
_generate({ type: "string" });
// Returns as a string

_generate({ type: "number" });
// Returns as an intengeter, or number

_generate({ type: "boolean" });
// Returns as a boolean

_generate({ type: "auto" });
// Returns as the detected data type
```
##### ***[!]** Remember: if you do not specify the data type, it will return as a string!*

Now onto settings!  To change what the password will look like, there are a few options.

One is to specify which characters can be used in the generation.  You can either send a string that includes all characters (order doesn't matter!), or choose a prepared value.

To change settings...
```js
_generate.set("characters", { type: "letters" });
// The character types are: "letters", "numbers", "symbols", "custom"
```
