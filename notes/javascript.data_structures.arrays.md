---
id: b2fbgyy39kk05enfzoipron
title: Arrays
desc: ''
updated: 1675125108464
created: 1670276602270
---
## Arrays in JavaScript

Arrays are ordered lists that can contain any data type. Array literals are represented by square brackets [] with comma delimited values, aka: elements.

Example of an array of numbers:
```js
> [1, 2, 3, 4, 5]
[ 1, 2, 3, 4, 5 ]
```

To access an array element, use its index value inside the brackets. Indexes are non-negative integers starting with zero.

Example of getting the first element:
```js
> [1, 2, 3, 4, 5][0] // or arr[0] if arr contains the array
= 1
```

Calling an array index equal to or greater than the array length returns 'undefined'.

## What is an Array?

Arrays are heterogeneous, meaning they can hold multiple data types, including primitives, objects and other arrays (called sub-arrays). Arrays are also ordered, with each element accessible through a unique index number. Array indices start with the number zero. So arrays are both indexed lists as well as ordered lists.

Array elements are accessed by their index number, in brackets. JavaScript provides the length of an array, useful for accessing the last element with the ```length``` property of an ```Array``` object.

Example:
```js
let names = ["Kevin", "Barb", "Tyler", "Norm"]
console.log(names[2]); // Tyler
console.log(names[names.length - 1]); // Norm is element 3 or length (4) - 1
```

## Modifying Arrays

Any array element can be replaced by re-assigning the element's index with a new value. Example: ```names[3] = "Gus"```

Values can be added to an array in a similar fashion, using ```names[names.length] and assigning a value to it.

Arrays declared as a ```const``` can't be reassigned, however the values in these arrays can be modified. To prevent this, use the ```Object.freeze()``` method on the array. This will ensure the array elements can not be changed unless dealing with nested arrays.

### Adding Array Elements with ```push```

Use the ```push()``` method to add an element to the end of an array. Pass the value of the element to the ```push()``` method. The method mutates the array and returns the new length property value of the mutated array.

### Adding Array Elements with ```concat```

Use the ```concat()``` method to concatenate two arrays and return a new array. This does not mutate the calling arrays.

Example:
```js
> array.concat(42, 'abc')
= [ 1, 4, 3, 10, 'a', null, 'xyz', 42, 'abc' ]

> array
= [ 1, 4, 3, 10, 'a', null, 'xyz' ]
```

### Removing Array Elements with ```pop```

Use the ```pop()``` method to remove and return the last element of an array. Since the array elements are modified, the ```pop()``` method mutates the caller.

### Removing Array Elements with ```splice```

Use the ```splice()``` method to remove and return a range of elements. The original array is mutated by the ```splice()``` method because those elements have been removed.

Example:
```js
let array = [1, 4, 3, 10, "a", null];

> array.splice(3, 2)
[ 10, 'a' ]

> array
= [ 1, 4, 3, null ]
```

## Iteration methods for Arrays

### Iterating arrays with ```forEach()```
This is similar to a ```for``` loop but generally preferred for style. A ```forEach()``` loop requires a callback function that is passed to ```forEach()``` as an argument. During each loop, the callback function is invoked one time for each element, with the element value passed as an argument. The return value of a ```forEach()``` loop is always ```undefined```.

Example:
```js
let array = [1, 2, 3];
array.forEach(function(num) {
  console.log(num); // on first iteration  => 1
                    // on second iteration => 2
                    // on third iteration  => 3
}); // returns `undefined`
```

This can also be done with an arrow function:

```array.forEach(num => console.log(num));```

### Transforming arrays with ```map()```

The ```map()``` function is more useful when creating a new array that contains modified elements from the original array. It reduces the risk of side effects because the original array is not mutated. Instead, it returns a new array, leaving the original intact.

Example:
```js
> numbers.forEach(num => squares.push(num * num));
> squares
= [ 1, 4, 9, 16, 1, 4, 9, 16 ]
```

