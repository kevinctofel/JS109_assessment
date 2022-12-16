---
id: mdy04wr8e2d19zfwp01y27n
title: Functions
desc: ''
updated: 1671219646225
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


