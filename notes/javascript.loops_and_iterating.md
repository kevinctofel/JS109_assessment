---
id: 1ee9kds01i6638da5ub39z2
title: Loops and Iterating
desc: ''
updated: 1678120754545
created: 1673922007182
---
## Loops and Iterating

### ```while``` Loops
Useful when you don't know how many iterations to loop.
While loops execute a code block until some condition is met. 
Example:
```js
let counter = 1;
while (counter <= 1000) {
  console.log(counter);
  counter = counter + 1;
}
```

### Looping Over Arrays With while
Example of iterating through an array of names with a ```while``` loop. While condition checks to see if we've iterated through all of the elements in the array, based on the length of the array. Note the index is incremented through each iteration of the loop.

```js
let names = ['Chris', 'Kevin', 'Naveed', 'Pete', 'Victor'];
let upperNames = [];
let index = 0;

while (index < names.length) {
  let upperCaseName = names[index].toUpperCase();
  upperNames.push(upperCaseName);
  index += 1;
}

console.log(upperNames); // => ['CHRIS', 'KEVIN', 'NAVEED', 'PETE', 'VICTOR']
```

### Using a ```do/while``` loop
Similar to a ```while``` loop but guarantees that it will always run through the loop at least one time. Why? Because the ```while``` condition happens after each loop is executed, not before it.

```js
let answer;
do {
  answer = prompt("Do you want to do that again?");
} while (answer === 'y');
```

### ```for``` loops
Another way to implement a loop by specifying an initialization variable, a condition to evaluate, and an increment or decrement of the loop variable.

Example of the above ```while``` loop rewritten as a ```for``` loop:
```js
let names = ['Chris', 'Kevin', 'Naveed', 'Pete', 'Victor'];
let upperNames = [];

for (let index = 0; index < names.length; index += 1) {
  let upperCaseName = names[index].toUpperCase();
  upperNames.push(upperCaseName);
}

console.log(upperNames); // => ['CHRIS', 'KEVIN', 'NAVEED', 'PETE', 'VICTOR']
```

### Controlling loops with ```continue``` and ```break```

```continue``` drops out of the current loop iteration and moves to the next one.
```break``` terminates the loop early; no additional iterations of that loop will run.

### Array Iteration

```forEach``` is built in to JavaScript as a array method for array iteration without a formal loop.

```js
let names = ['Chris', 'Kevin', 'Naveed', 'Pete', 'Victor'];

names.forEach(function(name) {
  console.log(name);
});
```

This example passes a function expression to the ```forEach``` method as an anonymous function, i.e.: it has no name. This can also be consolidated into an arrow function:

```js
let names = ['Chris', 'Kevin', 'Naveed', 'Pete', 'Victor'];

names.forEach(name => console.log(name));
```
Note that ```forEach``` doesn't return results of the function that it calls. It returns ```undefined```.

### Recursion

A recursive function is one that calls itself. Each call is added to the [call stack](./javascript.call_stack.md) as it waits for return values from the other function calls. Once the first function call returns a value the other functions on the stack can begin to return their values.

Example using a function to calculate a Fibonacci number:
```js
function fibonacci(number) {
  if (number < 2) return number; // 0 if number is 0, 1 if number is 1
  return fibonacci(number - 1) + fibonacci(number - 2);
}

console.log(fibonacci(6));  // => 8
console.log(fibonacci(20)); // => 6765
```

In this example, none of the calling functions know the return values until the conditional is met: ```if (number < 2)```. At that point, functions on the stack begin passing their return values to the calling functions and so on through the stack.

A recursive function must have a baseline condition, i.e.: the conditional in the above code.

### for/in and for/of loops

```for/in``` iterates over all enumerable properties of an object. Example:
```js
let obj = { foo: 1, bar: 2, qux: 'c' };
for (let key in obj) {
  console.log(key);
}
// Output:  foo
//          bar
//          qux
```
Note: Don't use ```for/in``` to iterate over arrays because the indices are stored as strings. Instead, use the ```for/of``` statement:
```js
let arr = [ 10, 20, 30 ]
for (let value of arr) {
  console.log(value);
}
// Output:  10
//          20
//          30
```
```for/of``` is also recommended when iterating through strings.


