# Functions

A function is a block of code that performs a specific task.

Functions help in writing modular, maintainable and reusable code.

**In JavaScript, functions are first-class citizens; this means that they can be assigned to variables, passed as arguments, returned from other functions, stored in data structures and even created dynamically.**

The basic syntax for declaring a function in JavaScript is as follows:
```js
function functionName() {
  // function body
}
```
```js
function printHello() {
  console.log("Hello, world");
}
```

To use a function, you must **call/invoke** the function as shown:
```js
function printHello() {
  console.log("Hello, world");
}

// calling/invoking a function
printHello();
```
# Parameters vs Arguments

A parameter is a variable declared in a function definition and acts as a placeholder for the value that will be passed to the function when the function is being called

An argument is the actual value passed to a function when it is called, it provides the data that the function or the method will operate on.
```js
function greet(name) { // name is a parameter
  console.log(`Hello ${name}`);
}

greet("John Doe"); // John Doe is an argument
```

# Function Return Values

A function can return a value using the return keyword.

```js
function add(number1, number2) {
  return number1 + number2;
}

let sum = add(35, 23);
console.log(sum);
```
# Categories of Functions

In programming, functions can be categorized as follows:
- Functions that don't take parameter(s) and don't return a value
- Functions that don't take parameter(s) but return a value
- Functions that take parameter(s) but don't return a value.
- Functions that take parameter(s) and return a value.

# Functions that don't take parameter(s) and don't return a value

As the name suggests, these functions don't take any parameter(s) and don't return any values.
```js
function add() {
  let a = 55;
  let b = 68;
  console.log(a + b);
}

add();
```

# Functions that don't take parameter(s) but return a value

These functions don't take any parameter(s), but they return a value.
```js
function add() {
  let a = 55;
  let b = 68;
  return a + b;
}

console.log(add());
```

# Functions that take parameter(s) but don't return a value

These functions take parameter(s) but don't return a value.
```js
function add(a, b) {
  console.log(a + b);
}
add(5, 3);
```
# Functions that take parameter(s) and return a value

These functions take in parameter(s) and return a value.
```js
function add(a, b) {
  return a + b;
}
console.log(add(5, 3));
```
# Types of functions in JavaScript

JavaScript has the following types of functions:
- Function declaration
- Function expression/anonymous function
- Arrow functions
- Immediately Invoked Function Expression (IIFE)
- Callback functions

# Function declaration
```js
function add(a, b) {
  console.log(a + b);
}

add(5, 2);
```

# Function expression/anonymous function

Involves saving a function to a variable.
```js
let add = function (a, b) {
  console.log(a + b);
}

add(5, 2);
```

# Arrow functions

Arrow functions were introduced in ES6 and are used to simplify how we write functions.
```js
let add = (a, b) => {
  return a + b;
}

console.log(add(5, 2));
```

**If an arrow function has only one line in the body, we can get rid of the curly braces**

This means that instead of:
```js
let add = (a, b) => {
  console.log(a + b);
}

add(5, 2);
```

We can write:
```js
let add = (a, b) => console.log(a + b);
```

If an arrow function has only one line of code in the body and that line happens to be a return statement, we can get rid of the `return` keyword:
```js
let add = (a, b) => a + b;

console.log(add(5, 2));
```
**If an arrow function has only one parameter, we can get rid of the parenthesis:**
```js
let square = number => number * number;

console.log(square(8)); // 64
```

# Immediately Invoked Function Expressions (IIFE)

These functions are executed immediately after being defined:
```js
(function () {
  console.log("Hello, World!");
})();
```
These functions can also take parameters:
```js
(function (a, b) {
  let sum = a + b;
  let product = a + b;
  console.log(`The sum of ${a} and ${b} is ${sum}`);
  console.log(`The product of ${a} and ${b} is ${product}`);
})(5, 6);
```

# Callback functions

Refer to functions passed as arguments to other functions.
```js
function greet(name, callback) {
  console.log(`Hello ${name}`);
  callback();
}

greet("Dennis", function () {
  console.log("Welcome back");
});
```


