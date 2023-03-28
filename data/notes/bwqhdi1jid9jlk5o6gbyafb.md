## Reassignment and mutation in JavaScript

### Reassignment
Changes the value assigned to a variable.
How? Variables point to the memory space where a value is stored, so we create a new memory space with a new value to reassign the variable. A reassigned variable points to this new memory space.

### Mutation
Change the value of the thing bound to the variable?
How? Mutation point to the values stored in memory, so we change the value where the variable points to. The variable still points to the same memory space.

Examples:
```js
let num = 3;              // A variable assigned to a primitive value
let arr = [1, 2, 3];      // A variable assigned to an array
let obj = { a: 1, b: 2 }; // A variable assigned to an object

num = 42;    // Reassignment
arr[1] = 42; // Reassignment of array element, but NOT the variable
             // The array referenced by arr is mutated!
obj.a = 42;  // Reassignment of object property, but NOT the variable
             // The object referenced by obj is mutated.

// You can still reassign the variables
arr = 42;                 // Reassignment; array is lost
obj = { b: 1, c: 2 }      // Reassignment: now refers to a different object
```

## Mutating the caller
Example of a non-mutating method, where the stored value of ```name``` remains unchanged:
```js
let name = "Pete Hanson";
console.log(name.toUpperCase()); // => 'PETE HANSON'
console.log(name);               // => 'Pete Hanson'
```
```toUpperCase()``` returns a new value but leaves the original value as is.

In contrast, the ```pop``` method mutates an array (the caller) and is therefore destructive:
```js
let oddNumbers = [1, 3, 5, 7, 9];
oddNumbers.pop();
console.log(oddNumbers); // => [1, 3, 5, 7]
```
Note that primitive values are immutable so their values never change; where they point to in memory can change, however. 

Functions can (but don't always) mutate arguments as well, although this applies only to global variables. Example:
```js
function changeFirstElement(array) {
  array[0] = 9;
}

let oneToFive = [1, 2, 3, 4, 5];
changeFirstElement(oneToFive);
console.log(oneToFive); // => [9, 2, 3, 4, 5]
```
## Key concept of mutation
Primitive values are immutable. That means their values never change; operations on immutable values always return new values. Operations on mutable values (arrays and objects) may or may not return a new value and may or may not mutate data.

