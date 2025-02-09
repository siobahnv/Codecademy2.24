# Codecademy Coursework

## Learn JavaScript / Introduction to JavaScript
console <br>
print / log <br>
"In JavaScript, the _console_ keyword refers to an object, a collection of data and actions, that we can use in our code." <br>
action / method <br>
- console.log() <br>
comments <br>
_single line comment //_ <br>
can be placed after / at end of line of code <br>
_/* multi-line comment */_ <br>
can be placed in the middle of a line of code <br>

### Data Types
8 fundamental data types: <br>
1. Number (including decimals)
2. BigInt: "Any number, greater than 253-1 or less than -(253-1), with n appended to the number: 1234567890123456n."
3. String (double or single quotes, single preferred)
4. Boolean (true / false)
5. Null (absense of value)
6. Undefined (does not exist)
7. Symbol (new type; complex)
8. Object (collections of related data)

First 7 are _primitive data types_ <br>

### Arithmetic Operators
"An _operator_ is a character that performs a task in our code." <br>
1. Add: +
2. Subtract: -
3. Multiply: *
4. Divide: /
5. Remainder: % aka modulo

string concatenation: + <br>
. dot operator <br>
methods <br>
instances <br>
argument <br>
```
instance.methodName();
```
built-in objects <br>
property <br>

### Resources
https://www.codecademy.com/resources/docs/javascript <br>
https://www.codecademy.com/workspaces/new (select JavaScript) <br>
https://www.codecademy.com/learn/introduction-to-javascript/modules/learn-javascript-introduction/cheatsheet <br>

## Variables <br>
"a _variable_ is a container for a value." <br>
Prior-ES6: _var_ <br>
Post-ES6-2015: _let_ and _const_ to create/declare variables <br>
_camel casing_ <br>
= _assignment operator_ <br>
value <br>

General naming rules: <br>
1. Cannot start with a numeral
2. Case-sensitive (myVar != myvar) 
3. != keywords 

_let_ and _variable_ can be reassigned different values and even created without a value, in that case the variable will be initilized with a value of "undefined" <br>
_const_, short for constant, cannnot be reassigned, will get a _TypeError_; will get a _SyntaxError_ if declared without a value <br>

### Operators
_mathematical assignment operators_ +=, -=, *=, /=<br>
_increment operator_ ++ <br>
_decrement operator_ -- <br>

_string concatenation_ + <br>
string interpolation and _template literals_ <br>
```
const myVar = 'example';
console.log(`Interpolating in a string literal ${myVar}.`);
// Output: Interpolating in a string literal example.
```
a template literal is wrapped by backticks ` <br>
a placeholder, ${myVar}, is used to interpolate <br>

_typeof operator_ can be used to check the data type of a variable's value <br>

## A Bit of History
JavaScript vs ECMAScript <br>
One can use JavaScript to create an app or program. <br>
One can use the guidelines of ECMAScript to create a new scripting language. <br>
ES6 or JavaScript ES6 or ES2015: refer to the sixth edition of ECMAScript released in 2015. <br>
ES6 is one of the biggest releases and is sometimes referred to as "Modern JavaScript" by developers. <br>

## Conditionals