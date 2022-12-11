---
id: javascript-data_types-numbers-nan
title: JavaScript Data_types Numbers Nan
desc: ''
updated: 1670725669197
created: 1670725669197
isDir: false
id_imported: b42gpdd9h3xmkz3nkhhl11m
title_imported: NaN
desc_imported: ''
updated_imported: 1669842924314
created_imported: 1669842663260
---
## NaN in JavaScript

NaN is a value that represents "Not a Number". 

Generally found in an illegal operation on numbers or trying to perform an operation on non-numeric data types.

It is of type Number:
```js
> typeof NaN
= 'number'
```

NaN is common when:
* Trying to divide by zero
* Find the square root of negative number
* Trying to convert a non-number value to a number

NaN is the only JavaScript value not equal to itself. 
```js
> let value = NaN;
> value === NaN         // We'll talk about this in a few minutes
= false

> NaN === NaN
= false
```

To determine if a value is NaN, use one of the two following methods:
```js
> let value = NaN;
> Number.isNaN(value)
= true

> Object.is(value, NaN)
= true
```
