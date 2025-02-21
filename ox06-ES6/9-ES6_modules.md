# ES6 Modules

ES6 introduced a modular system that allows JavaScript code to be split into multiple files, making it easier to manage and reuse code.

This system is built on exporting and importing functions, variables, or classes between files.

# Important Note About ES6 Modules

If you are using ES6 Modules in a browser, you need to add `type="module"` in the `<script>` tag, for example:
```js
<script type="module" src="main.js"></script>
```
To use ES6 modules in Node.js:
- Add "type": "`module`" in `package.json`.
- Use `.mjs` file extensions.

# Exporting and Importing in ES6 Modules

In ES6, you can export code from a module using either **named** exports or **default exports.**

**File:mathUtilis.mjs**
```js
export function add(a, b) {
  return a + b;
}

export function subtract(a, b) {
  return a - b;
}

export function multiply(a, b) {
  return a * b;
}
```
You can then import them in another module using the import keyword.

**File:index.mjs**
```js
import { add, subtract, multiply } from "./mathUtils.mjs";
console.log(add(5, 4));
console.log(subtract(5, 4));
console.log(multiply(5, 4));
```
**Note:you must precede the file name with `./` when importing

# Using aliases for imports

You can rename imports using the `as` keyword.
```js
import { add as sum, subtract as difference, multiply } from "./mathUtils.mjs";
console.log(sum(5, 4));
console.log(difference(5, 4));
console.log(multiply(5, 4));
```
# Importing everything (`*` as an object)

You can import all named exports as a single object:
```js
import * as MathUtils from "./mathUtils.mjs";
console.log(MathUtils.add(5, 4));
console.log(MathUtils.subtract(5, 4));
console.log(MathUtils.multiply(5, 4));
```
# Default Exports

Each module can have one default export, which can be imported with any name.

**File:logger.mjs**
```js
export default function log(message) {
  console.log(`Log: ${message}`);
}
```
Default exports don't need curly braces `{}` when importing.

You can import a default export with any name.

**File:index.mjs**
```js
import log from "./logger.mjs";

log("Hello, World");
```