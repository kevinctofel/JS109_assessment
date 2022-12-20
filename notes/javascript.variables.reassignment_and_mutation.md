---
id: bwqhdi1jid9jlk5o6gbyafb
title: Reassignment and mutation
desc: ''
updated: 1671557288303
created: 1671556958029
---
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

