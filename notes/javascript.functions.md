---
id: mdy04wr8e2d19zfwp01y27n
title: Functions
desc: ''
updated: 1671558761981
created: 1671218755744
---
## Functions in JavaScript

### Functions
Functions (or function objects) are defined by the ```function``` keyword. This can be skipped by using the name of a function when creating an arrow function, however.

```js
function say() {
  console.log("Hi!");
}
 // OR
 const say = () => {
  console.log("Hi!");
 }
 ```

To reduce ambiguity we say we are "invoking a function" rather than "calling a function".

### Arguments and Parameters
When we invoke a function we are passing arguments from outside the function's scope so the function can use the data. The arguments are objects or primitive values.

When defining a function, we declare any parameters the function accepts. Parameters are local variables initialized when the function is invoked. Therefore, when the function is complete, the parameters are destroyed.

You can pass more arguments than a function has parameters; they will be ignored. However, passing fewer arguments than a function requires causes an error as those missing parameters are assigned ```undefined```.

```js
function add(left, right) { // left & right are parameters here
  let sum = left + right;   // left & right are arguments here
  return sum;
}

console.log(add(3, 6, 5)); // 5 is ignored; prints 9
console.log(add(3));       // second argument missing; prints NaN
                           // 3 + undefined is NaN
```

### Return values
The ```return``` statement returns a result to the code that called a function.
Without a return statement, a JavaScript function will return ```undefined``` as the implicit return value.
Functions that always return a boolean value (true or false only) are predicates.

### Default parameters
You can set default parameters for functions invoked without any arguments provided by setting the parameter to a default value:
```js
function say(text = "hello") {
  console.log(text + "!");
}

say("Howdy"); // => Howdy!
say();        // => hello!
```

### Nested functions
Functions can be nested within other functions. Once the inner function completes, it and all of its local data, is destroyed.

### Function scope
Global variables are available to all code in a program, so any function has access to them. Functions can modify global variables.

Local variables defined inside of a function are only accessible within that function.

### Functions vs. methods
Functions pass arguments within their parenthesis. So too do methods, but methods are pre-defined functions on objects so you have to call a method on an object using the period.

## Function composition
JavaScript lets a function call as an argument to another function via function composition. This is because function calls always return a value.

Examples of passing a function call as an argument to the ```console.log()``` function:
```js
console.log(add(20, 45)); // => 65
console.log(subtract(80, 10)); // => 70
```

## Defining a function (three ways)
1. Create a function declaration and call the function.
2. Create a function expression by setting a variable name equal to a function declaration.
3. Use an arrow function, which is similar to option 2 but more concise. Arrow functions have implicit returns so you don't  need a ```return``` statement for a single expression. Example:
```js
let add = (a, b) => a + b; // this returns the value of a + b
```
