# Codecademy Coursework

## Learn Node.js
"Node.js is a powerful JavaScript runtime used to build efficient network applications." <br>

### Front and Back-end
"at its core, the _front-end_ is composed of JavaScript, CSS, HTML, and other _static assets_, such as images or videos. _Static assets_ are files that don’t change." <br>
_client-side_ development <br>
the _client_ may be the browser, another application, device, etc. <br>
"the _back-end_ consists of all the behind-the-scenes processes and data that make a website function and send resources to clients." <br>

_web server_, "is a process running on a computer that listens for incoming _requests_ for information over the internet and sends back _responses_." <br>
_protocol_ <br>
_HTTP protocol_ <br>
_HTTP request_ <br>
_static website_ <br>
_dynamic content_ <br>
_application server_, aka "application" <br>
_database_, "collections of information" <br>
two types: _relational databases_ and _non-relational databases_ (aka NoSQL) <br>
document storage model <br>
SQL, Structured Query Language <br>

_web API_ (Application Programming Interface) <br>
_authentication_ <br>
_authorization_ <br>

many options for back-end: PHP, Java, JavaScript, Python, etc. <br>
front-end is usually: HTML, CSS, and JavaScript <br>
back-end _frameworks_ <br>
_stack_ <br>

### JavaScript concepts for Node.js
_arrow expressions_ (ES6), () => { } <br>
```
const helloWorld = (name) => {
    console.log(`Hello ${name}.`)
};
helloWorld('JJ');
```

_synchronous code_ (blocking I/O) <br>
_asynchronous code_ (non-blocking I/O) <br>
_promises_, "A _Promise_ is a JavaScript object that represents the eventual outcome of an _asynchronous_ operation. A _Promise_ has three different outcomes: _pending_ (the result is undefined and the expression is waiting for a result), _fulfilled_ (the promise has been completed successfully and returned a value), and _rejected_ (the promise did not successfully complete, the result is an _error object_)." <br>
_.catch()_ method <br>
_async/await_, _async..await syntax_ <br>
```
const promiseObj = new Promise((resolve, reject) => {
    // code
});

promiseObj.then(message => { // code }).catch(error => { // code });

// async/await
const asyncFunction = async () =>{
    const finalResult = await promiseObj();
}
asyncFunction();
```

_setInterval()_ function, "executes a code block at a specified interval, in milliseconds" <br>
_setTimeout()_ function, "xecutes a code block after a specified amount of time (in milliseconds) and is only executed once" <br>

### JSON
