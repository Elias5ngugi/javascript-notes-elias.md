# Arrays

An array is a collection of elements stored at contiguous memory locations.

An array is a special variable, which can hold more than one value.

An array can hold many values under a single name, and you can access the values by referring to an index number.

# Creating an array

You can create an array in one of the following ways:
- An array literal
- The new `Array()` constructor.

**Using an array literal**
```js
const arrayName = [item1, item2, item3, ...];
```
**Example:
```js
const students = ["John", "Ken", "June", "Jack"];
```

# Using the new Array() constructor
```js
const arrayName = new Array(item1, item2, item3, ...)
```
**Example:
```js
const students = new Array("John", "Ken", "June", "Jack");
```
`new Array()` constructor can also be nested:
```js
const arr = new Array(1, 2, new Array(5, 6, new Array(30, 40)));
```
Always use array literal to create an array.

# Accessing array elements

You access an array element by referring to the **index number.**

The first element has index 0, the second element index 1, e.t.c.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students[0]); //John
console.log(students[1]); //Ken
console.log(students[2]); //June
```
# Basic Array methods

**Length of an array**

The `length` property returns the length (size) of an array.

The length of an array refers to the number of items in the array.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.length); // 4
```
`pop()`

The pop method removes the last item of an array.
```js
const students = ["John", "Ken", "June", "Jack"];
students.pop();
console.log(students); //[ 'John', 'Ken', 'June' ]
```
**Note:the pop method returns the element that was removed**

`push()`

The push method adds a new element at the end of the array.
```js
const students = ["John", "Ken", "June", "Jack"];
students.push("Nancy");
console.log(students); // ['John', 'Ken', 'June', 'Jack', 'Nancy']
```

You can also add multiple elements using the `push` method:
```js
const students = ["John", "Ken", "June", "Jack"];
students.push("Nancy", "Miriam", "Simon");
```

The push method returns the new length of the array.

`shift()`

The shift method removes the first element of an array.
```js
const students = ["John", "Ken", "June", "Jack"];
students.shift();
console.log(students); // ['Ken', 'June', 'Jack']
```
The shift method returns the element that was removed.

`unshift()`

The unshift method adds an element to the start of an array.
```js
const students = ["John", "Ken", "June", "Jack"];
students.unshift("Nancy");
console.log(students); // ['Nancy', 'John', 'Ken', 'June', 'Jack']
```
You can also add multiple elements using the `unshift` method:
```js
const students = ["John", "Ken", "June", "Jack"];
students.unshift("Nancy", "Miriam", "Simon");
```

`at()`

The at method returns an element at the specified index
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.at(2)); // June
console.log(students.at(0)); // John
```

`join()`

The join() method also joins all array elements into a string.

It behaves just like toString(), but in addition, you can specify the separator:
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.join("++")); // John++Ken++June++Jack
```

`concat()`

he concat() method creates a new array by merging (concatenating) existing arrays:
```js
const arr1 = ["jack", "franklin", "june"];
const arr2 = ["andrew", "alex", "ken"];
console.log(arr1.concat(arr2));
// [ 'jack', 'franklin', 'june', 'andrew', 'alex', 'ken' ]
```

`flat()`

The flat method converts a multidimensional array to a one-dimension array.
```js
const students = [
  ["jack", "franklin"],
  ["june", "andrew"],
  ["alex", "ken"],
];
console.log(students.flat());
// ['jack', 'franklin', 'june', 'andrew', 'alex', 'ken']
```

`indexOf()`

The `indexOf()` method is used to find the index of an element.

It returns -1 if the element is not found.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.indexOf("June")); // 2
```
`includes()`

Checks if an element exists in an array.

It returns true if it exists and false if it doesn't.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.includes("Ken")); // true
console.log(students.includes("Elvis")); // false
```

`reverse()`

everses the elements of an array.
```js
const students = ["John", "Ken", "June", "Jack"];
console.log(students.reverse());
```