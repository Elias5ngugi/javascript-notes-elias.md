# Sets

A set data structure in JavaScript is a data structure that represents a collection of unique values.

Unlike arrays which allow duplicate elements, sets only contain unique values.

# Properties of a set
- **Unique elements**: sets cannot contain duplicate elements.
- **No indexing**: elements in a set are not accessed by their position.
- **No order**: unlike arrays, elements in a set don't maintain their order.

# Creating a set

To create a set, use `new Set()`.
```js
const mySet = new Set([1, 2, "a", "John"]);
console.log(mySet);
```
# Set Methods

`add(value)`

Adds a new element with the specified value to the set.
```js
const mySet = new Set();
mySet.add("John");
mySet.add(44);
mySet.add(44);
mySet.add("Doe");
mySet.add(true);
mySet.add(true);
mySet.add(false);
console.log(mySet); // Set(5) { 'John', 44, 'Doe', true, false }
```
`has(value)`

Returns true if a specified value exists in a set, false otherwise.
```js
const mySet = new Set(["John", 44, "Doe", true, false]);
console.log(mySet.has("John")); // true
console.log(mySet.has("June")); // false
```
`size`

Returns the number of elements in a set.
```js
const mySet = new Set(["John", 44, "Doe", true, false]);
console.log(mySet.size); // 5
```