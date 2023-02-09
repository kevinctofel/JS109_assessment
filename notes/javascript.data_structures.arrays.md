---
id: b2fbgyy39kk05enfzoipron
title: Arrays
desc: ''
updated: 1675975678548
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

> let numbers = [1, 2, 3, 4]
> let squares = numbers.map(num => num * num);
> squares
= [ 1, 4, 9, 16 ]

> squares = numbers.map(num => num * num);
= [ 1, 4, 9, 16 ]
```
Although both methods work, ```forEach``` mutates the numbers array and returns ```undefined```, while ```map``` returns a new array.

### Filtering Arrays with ```filter```

Like ```map```, ```filter``` returns a new array. The difference is in the approach as ```filter``` returns truthy values from the callback function, which is generally some condition to return selected elements of the original array.

Example:
```js
> let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 1, 2]
> numbers.filter(num => num > 4)
= [ 5, 6, 7, 8, 9, 10 ]

> numbers
= [ 1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 1, 2 ]
```

Like ```map```, the ```filter``` method returns a new array and does not mutate the original array.

### Building New Values from Arrays with ```reduce```

This method reduces all elements in an array to a single value. It's useful for computing values in a single array, such as adding or subtracting them all together.

Example:
```js
> let arr = [2, 3, 5, 7]
> arr.reduce((accumulator, element) => accumulator + element, 0)
= 17

> arr.reduce((accumulator, element) => accumulator * element, 1)
= 210
```

The ```reduce``` method takes two arguments: a callback function and an initialized value typically called the accumulator. Think of it like setting a counter variable to zero to begin a counting computation. The accumulator value is returned to the callback iteratively. Above, the accumulator is initialized to 0 for an addition function, and 1 for a multiplication function.

## Some odd things about Arrays

Because of zero-indexing, the ```length``` property of an array is always one plus the highest index value.
Using the ```typeof``` operator on a array returns the value ```object```, not array. To verify if variable is referencing an array, use the ```Array.isArray(arr)``` method.

You can manually set or change the ```length``` of an array. Doing so with a value smaller than the current length value will truncate the elements after the final element of the new array. Doing so with a larger value creates more space by expanding the array size. However, the new indices are not initialized with any values, so they return ```undefined```.

Array indices can be negative numbers but the elements assigned to them are not counted in the ```length``` property.

You can use the ```Object.keys(arr)``` method to return the index values because arrays are objects.

## Nested arrays

An array that contains other arrays is called a nested array. When looking at an nested array value with a single index, it will return the entire nested array from the main array. By appending index values together, you can navigate and read through nested arrays.

Example:
```js
let scores = [['Kevin', 92], ['Barb", 86], ['Tyler', 73]];
console.log (scores[1][1]); // This returns Barb's score of 86
```

## Array equality

When comparing arrays for equality, you can't use the ```===``` operator because two different arrays point to to different memory locations, even if their values are the same. (Note: This is true of all objects in JavaScript)
Example:
```js
> [1, 2, 3] === [1, 2, 3]
= false
```
However, if you create a new variable that points to the variable of an existing array, these would be equal because both variables point to the same memory location.

To verify that two arrays hold the same element, you need to compare each array element from the first array to the corresponding element in another array.

## Other Array Methods

### ```Array.includes()```

The ```includes``` method checks to see if an array contains the argument value as an element. Example:

```js
> let a = [1, 2, 3, 4, 5]
> a.includes(2)
= true

> a.includes(10)
= false
```

### ```Array.sort()```

The ```sort``` method mutates the passed array so that its elements are in order. This occurs in place, so the return value is a reference to the same array. Remember, arrays are unordered lists, so ```sort``` will order an array list.

### ```Array.slice()```

The ```slice``` method returns the elements from a portion of an array. It takes two optional arguments: The index of where to start the sliced portion and the index of where to end the slice. The portion does not include the index value of the second parameter. Without any arguments passed, ```slice``` returns a new copy of the original array.

### ```Array.reverse()```

The ```reverse``` method is destructive because it mutates the original array and returns the elements in reverse order.

## Some exercises

1. Use the map function to create a new array that contains one element for each element in the original array. If the element is an even value, then the corresponding element in the new array should contain the string 'even'; otherwise, the element in the new array should contain 'odd'.

```js
let myArray = [
  1, 3, 6, 11,
  4, 2, 4, 9,
  17, 16, 0,
];

let newArray = myArray.map(element =>(element % 2 === 0 ? 'even' : 'odd'));
console.log(newArray);
```

2. Write a findIntegers function that takes an array argument and returns an array that contains only the integers from the input array. Use the filter method in your function.

```js
const findIntegers = (arrOfThings) => {
  return arrOfThings.filter(element => Number.isInteger(element));
}
let things = [1, 'a', '1', 3, NaN, 3.1415, -4, null, false];
let integers = findIntegers(things);

console.log(integers); // => [1, 3, -4]
```

