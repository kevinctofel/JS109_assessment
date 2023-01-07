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