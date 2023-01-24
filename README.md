# HTTP-Request-with-Javascript
How do I make an HTTP request in Javascript?

# Introduction 
JavaScript is a programming language that is primarily used to create interactive and dynamic web pages. It is a client-side scripting language, which means that it runs directly in the browser, rather than on a server. This allows for real-time updates, user input validation, and many other interactive features on web pages. JavaScript is also known as ECMAScript and is standardized by ECMAScript International.

JavaScript code can be added to an HTML page by placing it inside of a <script> tag, and it can also be included as an external file by linking to it with the src attribute.

JavaScript is also widely used outside of web development, for example, in the development of mobile apps with frameworks like React Native, desktop apps with Electron, and even for server-side development with Node.js.

In summary, JavaScript is a versatile, high-level programming language that allows developers to create interactive and dynamic web pages, and it's also used in a wide variety of other applications as well.

## Here we go
There are several ways to make an HTTP request in JavaScript, but the most commonly used method is the XMLHttpRequest object, which is built into most web browsers. Here is an example of how to use the XMLHttpRequest object to make a GET request to a server:

```
var xhr = new XMLHttpRequest();
xhr.open("GET", "https://example.com", true);
xhr.onreadystatechange = function() {
    if (xhr.readyState === 4 && xhr.status === 200) {
        console.log(xhr.responseText);
    }
};
xhr.send();
```

You can also use the Fetch API which is more modern, simple and easy to use.

```
fetch('https://example.com')
  .then(response => response.text())
  .then(data => console.log(data))
```

You can also use any other javascript libraries like Axios, jQuery etc.

```
axios.get('https://example.com').then(response => {
  console.log(response.data);
});
```
```
$.get('https://example.com', function(data) {
  console.log(data);
});
```

It's important to note that while XMLHttpRequest is supported by most web browsers, it is considered an "old" technology and the Fetch API is considered a more modern and simpler option.

