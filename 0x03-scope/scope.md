# Scope

**Scope** in JavaScript determines where variables are accessible.

It determines the accessibility (visibility) of variables.

JavaScript has the following types of scope:
- Global Scope
- Function Scope (local scope)
- Block Scope (introduced in ES6)
- Lexical scope

# Global Scope

A variable declared outside any function or block is considered globally scoped.

It is accessible anywhere in the JavaScript program.
```js
let age = 25;

function exampleFunction() {
  console.log(age); // accessible inside function
}

exampleFunction(); // 25
console.log(age); // accessible outside function too
```
# Function Scope

Variables declared inside a function are accessible only within that function.

They cannot be accessed outside the function.
```js
function exampleFunction() {
  let age = 25;
  console.log(age); // works inside the function
}

console.log(age); // ReferenceError: age is not defined
```
# Block Scope (`let` and `const`)

Before ES6, JavaScript only had global scope and function scope. The var keyword did not support block scope.

However, ES6 introduced `let` and `const`, which have block scope.

A block is any code inside curly brackets `{}` (e.g., in `if`, `for`, `while` statements).
```js
if (true) {
  let age = 25;
  console.log(age); // works inside the block
}
console.log(age); // age is not defined
```
Variables declared with `let` and `const` are only accessible inside the block they are declared in.

`var` does not follow block scope.

# Lexical Scope

Lexical Scope means that a function can access variables from its parent scope (e.g., parent function).
```js
function parentFunction() {
  let age = 25;
  function innerFunction() {
    console.log(age); // 25
  }
  innerFunction();
}

parentFunction();
```