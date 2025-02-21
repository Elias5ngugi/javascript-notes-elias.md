# Accessing/Finding Dom Elements

To access any element in an HTML page, we first start by accessing the `document` object.

The document object is the owner of all other objects on the page.

# Methods for accessing DOM elements

`document.getElementById(elementId)`

Finds an element with id equivalent to `elementId`.
```js
<button id="my-button">Click Me</button>
```
```js
const button = document.getElementById("my-button");
console.log(button); // <button id="my-button">Click Me</button>
```

`document.getElementsByTagName(name)`

Finds all the elements that match the tag name passed, e.g., finding all paragraph elements in a page.

It returns a NodeList of all elements that match the tag name passed.

You can index the specific element you want from this element the same way you would index an array.
```html
<p>Hello, World</p>
<p>JavaScript is awesome</p>
<p>JavaScript is great</p>
```
```js
const paragraphs = document.getElementsByTagName("p");
console.log(paragraphs); // [p, p, p]
```

`document.getElementsByClassName(className)`

Finds and returns a NodeList of all HTML elements with class attribute similar to the class specified.

You can index the specific element you want from this element the same way you would index an array.
```js
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```
```js
const texts = document.getElementsByClassName("text");
console.log(texts); // [p.text, p.text]
```

`document.querySelector(selector)`

Selects the first element in the document that matches a specified CSS selector, id or tag name.
```html
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```
```js
const firstText = document.querySelector(".text");
console.log(firstText);
```

`document.querySelectorAll(selector)`

Selects all elements in the document that match the specified class, id or tag name and returns a node list of them.
```html
<p class="text">Hello, World</p>
<p class="text">JavaScript is awesome</p>
<p>JavaScript is great</p>
```
```js
const paragraphs = document.querySelectorAll('p');
console.log(paragraphs); // [p.text, p.text, p]
```