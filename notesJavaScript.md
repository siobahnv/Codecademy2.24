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
"A conditional statement checks a specific condition(s) and performs a task based on the condition(s)." <br>

### If and If...Else and Else If Statements
```
if (true) {
  console.log('This message will print!'); 
}
// Prints: This message will print!

if (false) {
  console.log('The code in this block will not run.');
} else {
  console.log('But the code in this block will!');
}

// Prints: But the code in this block will!

let stopLight = 'yellow';

if (stopLight === 'red') {
  console.log('Stop!');
} else if (stopLight === 'yellow') {
  console.log('Slow down.');
} else if (stopLight === 'green') {
  console.log('Go!');
} else {
  console.log('Caution, unknown!');
}
```
_code block_, aka _block statement_, indicated by a set of curly braces {} <br>
_binary decisions_, yes-no <br>
Read from top to bottom, first condition evaluates to true executes. <br>

### Comparison Operators
Such as: <, >, <=, >=, ===, !== <br>
_identity operator_ === <br>

### Logical Operators
_and_ operator && <br>
_or_ operator || <br>
_not_ operator, aka _bang_ operator, !; reverses or negates the value <br>

### Truthy and Falsy
Falsy values include:
* 0
* Empty strings, "" or ''
* null
* undefined
* NaN (Not a Number)
_short-circuit evaluation_ <br>

### Ternary Operator
```
// if-else statement
let isNightTime = true;

if (isNightTime) {
  console.log('Turn on the lights!');
} else {
  console.log('Turn off the lights!');
}

// ternary operator statement
isNightTime ? console.log('Turn on the lights!') : console.log('Turn off the lights!');
```

### The switch keyword
```
let myVar = myValue;

switch (myVar) {
    case myValue0:
        code;
        break;
    case myValue1:
        code;
        break;
    case myValue2:
        code;
        break;
    default:
        code;
        break;
}
```
"Note: Without break keywords, the first matching case will run, but so will every subsequent case regardless of whether or not it matches—including the default." <br>

## Functions
"A function is a reusable block of code that groups together a sequence of statements to perform a specific task." <br>
_function declaration_, binds a function to a name, _identifier_ <br>
```
function identifier() {
    code;
}

function identifier(parameters=default) {
    code;
}

identifier(arguments);
```
_hoisting_ feature; can call a function before definted; not good practice <br>
A function _executes_ when it is _called_, _function call_. <br>
_parameters_ are placeholders that allow passing input(s) <br>
Values that are passed to a function as input(s) are called _arguments_. <br>
_default parameters_ can set a predetermined value if there is no argument or the argument is _undefined_ <br>
By default, the resulting value of a function is _undefined_. <br>
_return statement_ <br>
"When a return statement is used in a function body, the execution of the function is stopped and the code that follows it will not be executed." <br>

_helper functions_ <br>
_function expression_ <br>
"A function with no name is called an anonymous function." <br>
```
const identifierVar = function(parameters) {
    code;
};
```
"Unlike function declarations, function expressions are not hoisted so they cannot be called before they are defined." <br>

_arrow function syntax_, "fat arrow" () => notation <br>
```
const identifierVar = (parameters) => {
    code;
};
```
Many ways to refactor _arrow function syntax_. <br>
The most condensed form of _arrow function syntax_ is _concise body_. <br>
```
// ZERO PARAMETERS
const functionName = () => {};

// ONE PARAMETER
const functionName = param1 => {};

// MULTIPLE PARAMETERS
const functionName = (param1, param2) => {};

// SINGLE-LINE BLOCK
// implicit return
const functionName = param => code;

// MULTI-LINE BLOCK
const functionName = param => {
    code;
    return (optional_value);
};
```
_implicit return_, the keyword _return_ can be omitted. <br>

## Scope
"Scope defines where variables can be accessed or referenced." <br>
"Blocks help us group one or more statements together..." <br>
"In _global scope_, variables are declared outside of blocks." <br>
"We say that variable has _block scope_ because it is _only_ accessible to the lines of code within that block." <br>
"Variables that are declared with _block scope_ are known as _local variables_..." <br>
_global namespace_ <br>
_scope pollution_ <br>
"it’s best practice to not define variables in the global scope." <br>

## Arrays
_Arrays_ can store an _ordered_ list of any data types. <br>
_array literal_ <br>
_element_ <br>
```
[element0, element1, elementEtc]
```
_index_ <br>
_zero-indexed_, start counting from 0 <br>
_bracket notation_ <br>
```
// Named Array
let myArray = ['Index 0', 'Index 1', 'Index 2'];

// Acess element of array
myArray[index]
```
"Individual elements in arrays can also be stored to variables." <br>
"However, elements in an array declared with _const_ remain _mutable_. Meaning that we can change the contents of a _const_ array, but cannot reassign a new array or a different value." <br>
"One of an array’s built-in properties is _length_ and it returns the number of items in the array." <br>
_.length_ <br>
_dot notation_ <br>
_.push()_ , add items to the end of an array <br>
_mutates_ <br>
_destructive_ array method <br>
_.pop()_, removes the last item of an array; returns the value of the last element; mutates the array <br>
_non-mutating_ <br>
Read about more array methods: https://www.codecademy.com/resources/docs/javascript/arrays <br>

_pass-by-reference_ <br>
_nested array_ <br>
_chain_ indices using bracket notation <br>
```
const exampleNestedArr = [[1], [2, 3]];
// Output: 2
console.log(exampleNestedArr[1][0]);
```

## Loops
"A _loop_ is a programming tool that repeats a set of instructions until a specified condition, called a _stopping condition_ is reached." <br>
_iterate_, "to repeat" <br>
_for loop_ <br>
_iterator variable_ <br>
"A _for_ loop contains three expressions separated by ; inside the parentheses..." <br>
_initialization_ <br>
_stopping condition_ <br>
_iteration statement_ <br>
```
for (initialization; stopping condition; iteration statement) {
    code;
}
```
_infinite loop_ <br>
_i_ is a naming convention, often short-hand for _index_ <br>
_nested loop_ <br>

_while loop_ <br>
_test condition_, _stopping condition_ for a _while_ loop <br>
"The syntax of a _while_ loop is ideal when we don’t know in advance how many times the loop should run." <br>
```
initialization;
while(test condition) {
    code;
    iteration statement;
}
```

_do...while loop_ <br>
"A _do...while_ statement says to do a task once and then keep doing it until a specified condition is no longer met." <br>
```
initialization;
do {
    code;
    iteration statement;
} while (stopping condition);
```

_break_ keyword <br>
Can use breaks to add test condition other than the stopping condition. <br>
