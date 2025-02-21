# DOM Events

An event in the DOM is an action or occurrence that happens in the browser which the browser can respond to.

Events are triggered by user interactions such as clicks, key presses or mouse movements.

# Some popular DOM events

`onclick`

Triggered when an element is clicked.
```js
const btn = document.getElementById("btn");
btn.onclick = function () {
  console.log("Button Clicked");
};
```
`onmouseover`

Triggered when the mouse pointer moves over an element.

`onmouseout`

Triggered when the mouse pointer moves out of an element.

`onkeydown`

Triggered when a key is pressed down.


Usually called on the **document**, i.e., `document.onkeydown = function() {}`

`onkeyup`

Triggered when a key is released.

Usually called on the document, i.e., `document.onkeydown = function() {}`

`onload`

Triggered when the entire page has finished loading.

Called on **window**, i.e., `window.onload = function() {}`

`onfocus`

Triggered when an element gains focus
