# Loops

Loops enable you to execute a block of code multiple times.

The basic loops in JavaScript are:
- for loop
- while loop
- do while loop

# for loop

Used when the number of times the block of code should be executed is known.

The syntax is as follows:
```js
for (initialization; condition; update) {
    // code
}
```
- Initialization is used to initialize the variable used in the loop.
- Condition is used to evaluate the condition of the initial variable, if the condition returns true, the loop starts over again, if the condition returns false, the loop ends.
- Update is used to update the initialization variable.
```js
for (let i = 1; i <= 5; i++) {
    console.log("Iteration:", i);
}
```

# while loop

Runs as long as a specified condition remains true.
```js
while (condition) {
  // code block to be executed if condition is true
}
```
```js
let num = 1;

while (num <= 5) {
  console.log("Number ", num);
  num++;
}
```
# do while loop

Executes the loop at least once, even if the condition is `false` from the start.
```js
do {
  /* code of block that will be
     executed at least once even if
     condition is false */
} while (condition);
```
```js
let x = 1;

do {
  console.log("x ", x);
  x++;
} while (x <= 5);
```
# break and continue statements

`break` and `continue` statements are keywords that are always used within a loop.

# `break` statement

The purpose of a break statement is used when we want to terminate the running loop whenever any particular condition occurs

Whenever a `break` statement occurs, the loop breaks and stops executing.


The `break` statement exits the loop completely.
```js
for (let i = 0; i < 10; i++) {
  if (i == 5) {
    break;
  }
  console.log(i);
}
```
# `continue` statement

The `continue` statement is used when we want to skip a particular iteration.

Whenever we write `continue` statement, the whole code after that statement is skipped and the loop will go for the next iteration.

The `continue` statement skips the current iteration and moves on to the next iteration.
```js
for (let i = 0; i < 10; i++) {
  if (i == 5) {
    continue;
  }
  console.log(i);
}
```

