# Conditionals

Conditionals allow you to execute different blocks of code based on specific conditions

Conditional statements in JavaScript are:
- if statement
- if else statement
- if else ladder
- switch statement

# if statement

The if statement is used to execute a block of code if a specified condition is true.

The syntax is as follows:
```js
if (condition) {
  // block of code to be executed if the condition is true
}
```

Example in code:
```js
let age = 22;
if (age > 18) {
  console.log("You are an adult");
}
```
# if else statement

Executes the code in the `if` block when the condition is true, if the condition is false, the code inside the else block gets executed.
```js
if (condition) {
  // block of code to be executed if the condition is true
} else {
  // block of code to be executed if the condition is false
}
```
Example in code:
```js
let age = 16;
if (age > 18) {
  console.log("You are an adult");
} else {
  console.log("You are a child");
}
```
# if else ladder

Used when multiple conditions need to be checked sequentially.

The syntax is as follows:
```js
if (condition1) {
  // block of code to be executed if condition1 is true
} else if (condition2) {
  // block of code to be executed if condition1 is false and condition2 is true
} else {
  // block of code to be executed if both condition1 and condition2 are false
}
```
Example in code:
```js
let marks = 85;
if (marks >= 90) {
  console.log("Grade: A");
} else if (marks >= 80 && marks < 90) {
  console.log("Grade: B");
} else if (marks >= 70 && marks < 80) {
  console.log("Grade: C");
} else {
  console.log("Grade: F");
}
```
# Switch Statement

Used when a variable has multiple possible values. It’s cleaner than multiple if`..else` if conditions.

The syntax is as follows:
```js
switch (expression) {
  case value1:
    // block of code to be executed if expression === value1
    break;
  case value2:
    // block of code to be executed if expression === value2
    break;
  default:
  // block of code to be executed if expression doesn't match any case
}
```
Example in code:
```js
let day = "Monday";
switch (day) {
  case "Monday":
    console.log("Start of the work week.");
    break;
  case "Friday":
    console.log("Weekend is near!");
    break;
  case "Sunday":
    console.log("It's a rest day.");
    break;
  default:
    console.log("It's a regular day.");
}
```
# Ternary Operator

The ternary operator provides a concise way to write if-else statements in a single line.

The syntax is:
```js
condition ? expression if condition is true : expression if condition is false
```
Example in code:
```js
const age = 25;

age > 18 ? console.log("You are an adult") : console.log("You are a child");
```
