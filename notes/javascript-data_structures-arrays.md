---
id: javascript-data_structures-arrays
title: JavaScript Data_structures Arrays
desc: ''
updated: 1670725669197
created: 1670725669197
isDir: false
id_imported: b2fbgyy39kk05enfzoipron
title_imported: Arrays
desc_imported: ''
updated_imported: 1670615738521
created_imported: 1670276602270
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