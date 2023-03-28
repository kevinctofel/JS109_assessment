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
