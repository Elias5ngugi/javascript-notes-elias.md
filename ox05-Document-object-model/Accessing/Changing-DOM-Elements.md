# Changing DOM Elements

We can change the `content`, `attributes` and `styling` of DOM elements.

# Changing the content of HTML elements

`innerHTML`

Sets or gets the HTML content of an element.
```html
<div id="my-div">
    <h1>Hello, world</h1>
    <p>JavaScript is awesome</p>
</div>
```
```js
const div = document.getElementById("my-div");
console.log(div.innerHTML);
div.innerHTML = `<h1>New content</h1>`;
console.log(div.innerHTML);
```

`innerText`

Sets or get the text content of an element not preserving the HTML tags.
```html
<div id="my-div">
    <h1>Hello, world</h1>
    <p>JavaScript is awesome</p>
</div>
```
```js
const div = document.getElementById("my-div");
console.log(div.innerText);
div.innerText = "New content";
console.log(div.innerText);
```
`textContent`

Sets or gets the text content of an element and its descendants without preserving the HTML tags.

It is more consistent across browsers compared to `innerText`.

# Changing the attribute of HTML elements
- We can use `element.attribute = value`.
```html
<h1 class="title" id="title">Hello, world</h1>
```
```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.id = "awesome-title";
console.log(title); // <h1 class="title" id="awesome-title">Hello, world</h1>
```
- We can also use `element.setAttribute("attribute", "value")`
```html
<h1 class="title" id="title">Hello, world</h1>
```
```js
const title = document.getElementById("title");
console.log(title); // <h1 class="title" id="title">Hello, world</h1>
title.setAttribute("id", "awesome-title");
console.log(title);
```

# Changing the styling of HTML elements

We can use `element.style.property = "value".`

It is important to input the value in double quotes even if it is a number.
```js
const title = document.getElementById("title");
title.style.border = "3px solid red";
title.style.fontSize = "48px";
title.style.borderRadius = "5px";
```

**Changing styling in JavaScript using CSS classes**
- `element.classList.add()`: adds one or more class names to an element without removing the existing classes.
- `element.classList.remove()`: removes one or more classes from an element.
- `element.classList.toggle()`: toggles the specified class, it is present, it is removed, if it is absent, it is added.
- `element.classList.contains()`: returns true if an element contains the specified class(es), false otherwise.
- `element.classList.replace()`: replaces an existing class with a new class.
- `element.style.setProperty()`: sets a CSS property on an element (first parameter) and its value (second parameter).