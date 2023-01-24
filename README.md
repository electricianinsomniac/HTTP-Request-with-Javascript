# HTTP-Request-with-Javascript
How do I make an HTTP request in Javascript?

# Introduction 

## here we go
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

