# Template literals

Template literals (also known as template strings) were introduced in ES6 to make working with strings more flexible and readable.

They allow:
- Multi-line strings without `\n.`
- String interpolation (injecting variables to strings).
- Embedded expressions.
- e.t.c.

Template literals use backticks instead of single or double quotes.

# String interpolation: Injecting variables into strings

Before ES6, inserting variables into a string required concatenation (+), which was cumbersome.

With template literals, introduced in ES6, this has been made easier:

**Before template literals:**
```js
const username = "Dennis";
const age = 25;

console.log("My name is " + username + " and I am " + age + " years old.");
// My name is Dennis and I am 25 years old.
```

**With template literals:**
```js
const name = "Dennis";
const age = 25;

console.log(`My name is ${name} and I am ${age} years old.`);
// My name is Dennis and I am 25 years old.
```
# Multi-line strings (No need for \n)

Before ES6, multi-line strings required `\n` or joining with `+:`
```js
const multiLine = "This is line 1\n" + "This is line 2\n" + "This is line 3";

console.log(multiLine);
/*
This is line 1
This is line 2
This is line 3
*/
```
```js
const multiLine = `This is line 1
This is line 2
This is line 3`;

console.log(multiLine);
/*
This is line 1
This is line 2
This is line 3
*/
```
# Expressions inside template literals

Template literals can evaluate expressions directly inside `${}`.
```js
let a = 10;
let b = 20;

function product(number1, number2) {
  return number1 * number2;
}

console.log(
  `The sum of ${a} and ${b} is ${a + b} and the product is ${product(a, b)}`,
);
```
