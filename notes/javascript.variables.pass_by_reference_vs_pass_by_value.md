---
id: ns9d3wjcc122f106hw5lwtl
title: Pass by reference vs pass by value
desc: ''
updated: 1680020572798
created: 1680019390923
---
## Pass by Value

Passing a variable by value to a function means the function can't set the original variable to a different value. The original variable will still contain the original value.

Example:
```js
function changeName(name) {
  name = "bob"; // does this reassignment change the variable outside the function? NO
}

function anotherFunction() {
  let name = "jim";
  changeName(name);
  console.log(name); // => logs 'jim'
}

anotherFunction();
```

## Pass by Reference

Example of pass by reference:
```js
function capitalize(names) {
  for (let index = 0; index < names.length; index++) {
    names[index] = names[index][0].toUpperCase() + names[index].slice(1);
  }
}

let names = ["chris", "kevin", "naveed"];
capitalize(names);
console.log(names); // => ['Chris', 'Kevin', 'Naveed']
```

Similar example where the function doesn't change the values
```js
function capitalize(names) {
  return names.map(name => name[0].toUpperCase() + name.slice(1));
}

let names = ["chris", "kevin", "naveed"];
capitalize(names); // returns ['Chris', 'Kevin', 'Naveed']
console.log(names); // => ['chris', 'kevin', 'naveed'] // The original object still has the original values because the capitalize() function doesn't mutate it. Instead, it returns a new array object.
```

## How JavaScript manages pass by value vs pass by reference

Passing primitive values to functions is pass by value so functions don't mutate the primitive values.

JavaScript always treats objects passed to functions as pass by reference, and therefore, can mutate those objects.

**When an operation within the function mutates its argument, it affects the original object.**

Functions that mutate their callers are called destructive functions or methods. Example:
```js
function addNames(arr, name) {
  arr.push(name);
}

let names = ["bob", "kim"];
addNames(names, "jim");
console.log(names); // => [ 'bob', 'kim', 'jim' ]
```

Reassignment is not a destructive operation. Example:
```js
function addName(arr, name) {
  arr = arr.concat([name]); // not destructive
}

let names = ["bob", "kim"];
addName(names, "jim");
console.log(names); // => [ 'bob', 'kim', ]
```

Similar example with a destructive function:
```js
function addNames(arr, name) { 
  arr = arr.push(name); // destructive through mutation
}

let names = ["bob", "kim"];
addNames(names, "jim");
console.log(names); // => [ 'bob', 'kim', 'jim' ]
```

## Return values

Values returned by functions can be pass by value or pass by reference.

Example of pass by value because the caller passes a primitive:
```js
function foo(number) {
  return number;
}

let number = 1;
let newNumber = foo(number);
console.log(number);    // 1
console.log(newNumber); // 1

number = 3;
console.log(number);    // 3
console.log(newNumber); // 1
```

Example of pass by reference because the caller passes an object:
```js
function bar(array) {
  return array;
}

let array = [1, 2, 3];
let newArray = bar(array);
console.log(array === newArray); // true (they are same object)

array.push(4);
console.log(array);    // [ 1, 2, 3, 4 ]
console.log(newArray); // [ 1, 2, 3, 4 ]
```

## Assignment

Pass by value and pass by reference don't apply to assignment of variables.
