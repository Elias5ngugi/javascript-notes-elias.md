# let and const for block scoped variables

Block scope refers to the scope of variables within a pair of curly braces {} such as within loops, conditionals, or functions.

Before ES6, JavaScript only had function scopes and global scope which led to issues like variable hoisting.

Variables declared with `let` keyword are only accessible within the block they are defined.

Unlike `var`, `let` declarations are not hoisted. Hoisting is JavaScript's default behavior of moving functions and variable declarations to the top of their scope meaning that function declarations can be called before they appear in the code and variable declarations (not assignments) are moved to the top of their scope.

`const` allows you to declare variables that are block scoped but are read-only.

The value of a `const` variable cannot be changed after assignment.

Variables declared with the `const` keyword must be initialized, on the other hand, variables declared with the `let` keyword can go uninitialized.