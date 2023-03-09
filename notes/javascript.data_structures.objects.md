---
id: xfj1cw13flf2irwhxy4kz97
title: Objects
desc: ''
updated: 1678385050265
created: 1670276925220
---
## Objects in JavaScript

Objects can be a dictionary-like structure with keys matching unique values, i.e.: A key-value pair.

Object literals are created with curly braces, {} , and keys separated from values with a colon, : Multiple key-value pairs are comma separated:
```js
> { dog: 'barks', cat: 'meows', pig: 'oinks' }
= { dog: 'barks', cat: 'meows', pig: 'oinks' }
```

Values can be retrieved by their keys:
```js
> ({ dog: 'barks', cat: 'meows', pig: 'oinks' })['cat']
= 'meows'
// or objects variable name and key in brackets
// animals['cat'];
```

Other languages have key-value pairs but refer to them as dictionaries (Python?), associative arrays, maps and hashes.

Object keys in JavaScript are strings (quotes are not needed) or symbols. Values can be any type.Example of creating an object with object literal syntax:
```js
> let person = { name: 'Jane', age: 37, hobbies: ['photography', 'genealogy'] }
```

Object values are accessed with dot notation or bracket notation. The latter is required when a variable stores a key name.
```js
> person.name                 // dot notation
= 'Jane'

> person['age']               // bracket notation
= 37
```

To remove a value from an object, you can ```delete``` the object's key for that value. Doing so returns ```true``` unless the object property can't be deleted. Note: 'property' typically refers to an object key.

When using ```const``` to declare and initialize an object, you can't change what the variable refers to. You can modify that object's properties and property values.

```Object.freeze()``` prevents an object's properties from modification. This only works one level deep, however. Nested arrays or objects must be frozen to prevent modification.

## Objects vs primitives

Objects include simple objects, arrays, dates, functions and more. They're comprised of primitive values or other objects and are usually mutable.

Primitive values are always [immutable](https://developer.mozilla.org/en-US/docs/Glossary/Immutable) and considered atomic, i.e.; indivisible.



### Functions are objects

Variables can be assigned to functions.
Example:
```js
function hello() {
  console.log("Hello there!");
}

hello();            // Prints "Hello there!"

let greet = hello;  // `greet` now points to the `hello` function
greet();            // Prints "Hello there!"
```

Functions can be passed to other functions and can be returned by other functions. Example of passing a function to another function as an argument:
```js
Array.prototype.forEach = function(callback) {
  for (let index = 0; index < this.length; index += 1) {
    callback(this[index]);
  }
}

let array = [1, 2, 3];
array.forEach(function callback(value) { console.log(value); })
```

### What things aren't objects or primitives?

Anything that isn't data or a function isn't an object nor a primitive value:
- Variables and function names
- Statements (if, return, try, while, break)
- Keywords (new, function, let, const, class)
- Comments

## Prototypes

JavaScript objects can inherit properties from other objects.

The ```Object.create()``` method creates a new object that inherits properties from an existing object. Example where ```bob``` is the prototype for the ```studentBob``` object:
```js
let bob = { name: 'Bob', age: 22 };
let studentBob = Object.create(bob);
studentBob.year = 'Senior';

console.log(studentBob.name); // => 'Bob'
```

## Iteration

### The for/in loop

Similar to a standard ```for``` loop but simpler as it iterates over all keys in an object. Example:

```js
let person = {
  name: 'Bob',
  age: 30,
  height: '6 ft'
};

for (let prop in person) {
  console.log(person[prop]);
}                             // => Bob
                              //    30
                              //    6 ft
```

### Object keys

```Object.keys()``` returns all of an object's own keys as an array. It does not return keys from any prototype objects.

## Common Operations and Methods

```Object.values()``` returns an object's own properties in an array. Example:
```js
let person = { name: 'Bob', age: 30, height: '6ft' };
let personValues = Object.values(person);
console.log(personValues); // => [ 'Bob', 30, '6ft' ]
```

```Object.entries()``` returns the keys and values of an object in a nested array. Example:
```js
let person = { name: 'Bob', age: 30, height: '6ft' };
console.log(Object.entries(person)); // => [[ 'name', 'Bob' ], [ 'age', 30 ], [ 'height', '6ft' ]]
```

```Object.assign()``` merges the keys and values of two or more objects into a single object. This mutates the first object so that it contains the merged object. Example:
```js
> let objA = { a: 'foo' }
= undefined

> let objB = { b: 'bar' }
= undefined

> Object.assign(objA, objB)
= { a: 'foo', b: 'bar' }
```

## Objects vs. Arrays

How to choose between an object and an array for storing data:
- If the values have individual names or labels, use and object.
- If order matters, choose an array.
- For stack and queue types of data, choose an array.

NOTE: JavaScript will coerce non-string values when using them as object keys.






