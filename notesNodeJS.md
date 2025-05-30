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
"_JSON_, or _JavaScript Object Notation_, is a popular, language-independent, standard format for storing and exchanging data." <br>
"Trailing commas are forbidden." <br>
"JSON property names must be in double-quoted <font color="#800080">(" ")</font> text even though JavaScript names do not hold by this stringency." <br>
Doesn't cover every data type, such as dates/times: https://www.iso.org/iso-8601-date-and-time-format.html <br>

### Intro
"_Node.js_ is a JavaScript _runtime_, or an environment that allows us to execute JavaScript code outside of the browser." <br> 
"A “runtime” converts code written in a _high-level_, human-readable, programming language and compiles it down to code the computer can execute." <br>

#### Resources
https://developer.mozilla.org/en-US/docs/Web/JavaScript <br>
https://nodejs.org/api/ <br>

"_REPL_ is an abbreviation for read–eval–print loop." <br>
"When you install _Node_, it comes with a built-in JavaScript _REPL_. You can access the _REPL_ by typing the command _node_ (with nothing after it) into the terminal and hitting _enter_." <br>
.editor, "editor" mode, control + d to _enter_<br>
"Each session of the REPL has a _single shared memory_; you can access any variables or functions you define until you exit the REPL." <br>
_Node global object_ <br>

.js extension <br>
_modularity_ <br>
_modules_ <br>
_require()_ function <br>
_core modules_, examples: events, util, console, process, os <br>
lib/ folder <br>
