---
id: javascript-data_types-typeof
title: JavaScript Data_types Typeof
desc: ''
updated: 1670725669198
created: 1670725669198
isDir: false
id_imported: 5skg0v7cisye4d9ntvrceif
title_imported: Typeof
desc_imported: ''
updated_imported: 1669842126782
created_imported: 1669841958268
---
## Typeof operator in JavaScript

The typeof operator returns the data type of an operand.

Example:
```js
> typeof 1
= 'number'

> typeof 'foo'
= 'string'

> typeof true
= 'boolean'

> typeof undefined
= 'undefined'

> typeof null
= 'object' // That's just weird

> typeof [1, 2, 3]
= 'object' // You'd expect this to be an array, but arrays are objects
```


Since typeof is an operator and not a method, it doesn't use () like a method.