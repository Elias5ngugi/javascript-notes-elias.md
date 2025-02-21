# Rest Operator

The rest operator (`...`) is used to collect multiple elements into a single array or object.

Rest operator is used in array destructuring (more about this later).

# Rest Operator Use Cases

**Rest in function parameters**

When a function has multiple parameters but we don’t know how many arguments will be passed, we can use the rest operator.
```js
function myFunction(...numbers) {
  console.log(numbers);
}

add(5, 6);
add(10, 14, 23, 12, 9);
add(2);
```