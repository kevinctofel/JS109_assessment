---
id: b2fbgyy39kk05enfzoipron
title: Arrays
desc: ''
updated: 1670615738521
created: 1670276602270
---
## Arrays in JavaScript

Arrays are ordered lists that can contain any data type. Array literals are represented by square brackets [] wit comma delimted values, aka: elements.

Example of an arry of numbers:
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