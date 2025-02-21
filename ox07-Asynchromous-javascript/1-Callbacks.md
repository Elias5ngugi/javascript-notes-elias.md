# Callbacks

Callbacks are one of the solutions for asynchronous programming in JavaScript.

Let's say you are building a web application where you need to fetch user data from a database or an API. You might have written your code like this:
```js
function fetchData() {
    let data = { username: "John Doe", role: "Admin" };
    return data;
}

function showData(data) {
    console.log(`Username is ${data.username} and role is ${data.role}`);
}

const userData = fetchData();
showData(userData);
```
`fetchData()` retrieves user data and returns it immediately.

`showData(userData)` then logs the user's details.

This works fine for **synchronous operations**, where `fetchData()` instantly provides the data. But what if fetching data takes time, like when calling an API or reading from a database?

Imagine fetchData() is modified to simulate an API request using setTimeout:
```js
function fetchData() {
  setTimeout(() => {
    let data = { username: "John Doe", role: "Admin" };
    return data;
  }, 2000);
}

function showData(data) {
  console.log(`Username is ${data.username} and role is ${data.role}`);
}

const userData = fetchData();
showData(userData);
```
`setTimeout()` delays execution of the function, making it asynchronous.

`fetchData()` does not wait for the data to be ready—it returns undefined immediately.

When `showData(userData)` runs, `userData` is `undefined`, leading to errors.

**The solution here is to use callbacks**

A **callback function** is a function passed as an argument to another function, ensuring that execution happens only after the asynchronous operation is complete.
```js
function fetchData(callback) {
  setTimeout(() => {
    let data = { username: "John Doe", role: "Admin" };
    callback(data);
  }, 2000);
}

fetchData(function (data) {
  console.log(`Username is ${data.username} and role is ${data.role}`);
});
```
Now that we understand how callbacks solve the problem of asynchronous execution, let’s look at callback hell, a situation where too many nested callbacks make the code unreadable and hard to manage.

Assuming we are fetching data with multiple data points:
- fetch user data (e.g., username and role)
- Fetch user's posts after getting user data
- Fetch comments on a post after retrieving posts
- Display all the data after everything is fetched.

Using callbacks, your code will look like this:
```js
function fetchUser(callback) {
  setTimeout(() => {
    console.log("Fetched user data");
    let user = { username: "John Doe", role: "Admin" };
    callback(user);
  }, 2000);
}

function fetchPosts(user, callback) {
  setTimeout(() => {
    console.log(`Fetched posts for ${user.username}`);
    let posts = ["Post 1", "Post 2", "Post 3"];
    callback(posts);
  }, 2000);
}

function fetchComments(post, callback) {
  setTimeout(() => {
    console.log(`Fetched comments for ${post}`);
    let comments = ["Nice post!", "Great work!", "Interesting read"];
    callback(comments);
  }, 2000);
}

// Callback Hell (Nested Callbacks)
fetchUser((user) => {
  fetchPosts(user, (posts) => {
    fetchComments(posts[0], (comments) => {
      console.log(`User: ${user.username}, Role: ${user.role}`);
      console.log(`Posts: ${posts}`);
      console.log(`Comments on first post: ${comments}`);
    });
  });
});
```

The problems with the code above are:

- The indentation (callback hell) keeps increasing making the code harder to read.
- **Difficult debugging**: If something goes wrong, finding the issue in nested callbacks is frustrating.
- If we add more steps (e.g., fetch likes, fetch friends), the nesting increases further.

To avoid callback hell, we can replace callbacks with Promises, which provide better structure and readability.
