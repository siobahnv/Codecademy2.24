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
"JSON property names must be in double-quoted _(" ")_ text even though JavaScript names do not hold by this stringency." <br>
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

"Since _console_ is a _global module_, its methods can be accessed from anywhere, and the _require()_ function is not necessary." <br>

"a _process_ is the instance of a computer program that is being executed" <br>
_process_ is a global module <br>
process.env <br>
NODE_ENV, production, development <br>
process.memoryUsage() <br>
process.memoryUsage().heapUsed <br>
process.argv <br>
https://nodejs.org/api/process.html <br>

os module is not global <br>
```
const os = require('os');
```

utility functions <br>
util module <br>
util.promisify() <br>

### Setting Up Node Locally
https://www.codecademy.com/article/command-line-setup <br>
https://nodejs.org/en/ <br>
Node "LTS", Long Term Support <br>
```
which node
node -v
```

### Getting Started with Node Package Manager
Node Package Manager (NPM) <br>
_dependencies_, third-party modules <br>
_package_, "a third-party module wrapped up with the list of that module’s own dependencies" <br>
_package manager_, downloads & installs, checks for vulneriblities & updates, handles sub-dependencies, and removes unneeded files; "Provides a repeatable and consistent process of installing dependencies" <br>
_npm_, command-line tool <br>

```
// Follow the prompts & a package.json file will be generated
npm init

// To skip the prompts
npm init -y
```
https://www.npmjs.com/ <br>
_nodemon_ package <br>
```
// i is actually an alias for install, and either npm i or npm install can be used
npm i nodemon
```
"The _npm i <package name>_ command installs a package _locally_ in a folder called **node_modules/** which is created in the project directory that you ran the command from. In addition, the newly installed package will be added to the _package.json file_" <br>
development dependencies <br>
```
// To install nodemon as a development dependency, we can add the flag --save-dev, or its -D alias.
npm install nodemon --save-dev
```
"_Development dependencies_ are listed in the "devDependencies" field of the package.json file." <br>
"Like local packages, _development dependencies_ are also stored in the local **node_modules/** folder." <br>

installed _globally_, available system-wide <br>
ex. http-server package <br>
```
npm install http-server -g
```
"packages installed _globally_ will not be listed in a projects **package.json** file and they will be stored in a separate global **node_modules/** folder." <br>

```
// automatically install all packages listed as dependencies or development dependencies
npm i

// leave out development dependencies
npm i --production
```
"Because of this convenient command, it is recommended that you do not include your local **node_modules/** folder in any repository that you use to store and share your code to avoid taking up precious storage resources." <br>

### Implementing Modules in Node
"module" and "file" are often used interchangably <br>
separation of concerns <br>
Node runtime envirnoment with built-in functions: module.exports and require() <br>
browser-based runtime environment, ES6 import/export syntax <br>

#### Resources
https://www.codecademy.com/article/implementing-modules-using-es-6-syntax <br>
https://www.codecademy.com/article/introduction-to-javascript-runtime-environments <br>

exports, named functions vs anonymous functions <br>
Can use object destructuring to extract only needed functions from modules instead of everything <br>
```
const { function } = require('./module.js');
```

### Node Modules
https://nodejs.org/docs/latest-v14.x/api/modules.html <br>

### Node.js Essentials
core Node.js modules: events, error, buffer, fs, and timer <br>
event-driven architecture <br>
.on() method <br>
_listener_ callback function <br>
.emit() method <br>

input/output <br>
"thin wrapper" <br>
console.log(), .stdout.write() of process object <br>
stdout = standard output <br>
stdin.on(), instance of EventEmitter of process module <br>

error module: EvalError, SyntaxError, RangeError, ReferenceError, TypeError, and URIError <br>
error module is within the global scope <br>
_error-first callback functions_ <br>

Buffer module is within the global scope as well <br>
"A Buffer object represents a fixed amount of memory that can’t be resized. Buffer objects are similar to an array of integers where each element in the array represents a byte of data. The buffer object will have a range of integers from 0 to 255 inclusive." <br>
Buffer methods include: .alloc(), .toString(), .from(), and .concat() <br>

filesystem <br>
sandboxing <br>
fs core module, "was modeled after the _POSIX_ standard for interacting with the filesystem" <br>
"Each method available through the fs module has a synchronous version and an asynchronous version." <br>
.readFile() method <br>

_stream_ <br>
_readline_ core module <br>
.createInterface() <br>
.createWriteStream() <br>

_timer_ module, global <br>
Node.js event loop <br>
