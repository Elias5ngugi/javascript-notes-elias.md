# Including javascript
- Internal javascript
- External javascript

<h1>Internal javascript</h1>

Here, javascript is written inside a `<script>` tag within the HTML file 

```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
  </head>
  <body>
    <h1>JavaScript</h1>
    <script>
      console.log("Hello, world!");
      console.log("JavaScript is fun")
    </script>
  </body>
</html>
```
Placing scripts at the bottom of the <body> element improves the display speed; because script interpretation slows down the display.

# External javascript
Here, JavaScript is stored in a separate `.js` file and linked to the HTML document using the `<script>` tag with a src attribute.

index.html
```html
<!doctype html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Document</title>
    <script src="app.js"></script>
  </head>
  <body>
    <h1>JavaScript</h1>
  </body>
</html>
```
app.js
```js
console.log("Hello, world!");
console.log("JavaScript is fun");
```
# Optimizing script loading
JavaScript can block page rendering if not loaded correctly.

The browser parses our HTML code line by line and when it comes across a resource that needs to be downloaded to the page e.g. an image, it sends a request to the server to download this resource.

However, when it comes across the script tags to download JavaScript, it stops until the JavaScript has been downloaded, it then executes this JavaScript after it has been downloaded and then continues parsing the HTML.

This can end up hurting performance.

To improve performance, use:

1. **defer** keyword
- This ensures that scripts are loaded after the HTML is fully loaded.
- Example:
```js
<script src="app.js" defer></script>
```
2. The **async** keyword
- Loads scripts asynchronously and runs them as soon as they are downloaded.
- May execute JavaScript out of order.
```js
<script src="script.js" async></script>
```
3.The script tag at the end of the page
-Put the script tag at the very end of the page before the closing body tag.
```js
  ...
    <script src="app.js"></script>
</body>
</html>
```
Avoid using the async keyword unless you are absolutely sure that it fits your needs, stick to the defer keyword or using the script tag at the end of the HTML document before the closing body tag.

