---
id: r5xdkanjp8myc7euvod3v1c
title: Coercion
desc: ''
updated: 1679192491916
created: 1670275182089
---
## Explicit Coercion

If we want to change a data type, such as a string of numbers to a Number type, we perform an explicit type coercion.

- String to Numbers

Use the Number function to coerce a string to a number:
```js
> Number('1')
= 1
```

The Number function accepts a string value argument, returning a number if the string is comprised of valid numeric data. 

**If the string doesn't have valid numeric data, ```Number()``` will return ```NaN```**

**Coercing an empty string to a number returns a ```0```**

**Coercing a boolean value from ```true``` returns a ```1``` while coercing ```false``` returns a ```0```**

- parseInt() function alternative

Similar to the Number() function for coercion but works with a mix of string data comprised of numbers and non-numeric characters. 

**```parseInt()``` will convert string numbers until it reaches an invalid character.**

```js
> parseInt('12xyz')
= 12
```
Note that if you pass a fractional character to parseInt() it will only return the integer value, not any decimal values less than 1.
```js
> parseInt('3.1415')
= 3
```

**```parseInt()``` can accept a second argument called the radix; this indicates the base of the number argument, i.e.: radix of 2 = base 2**

- parseFloat() alternative

However, the parseFloat() function will handle fractional numbers for explicit coercion.
```js
> parseFloat('12.5foo')
= 12.5
```

- Numbers to strings

To explicitly coerce numbers into a string data type, use the String() function.

** This function can be used on ```undefined``` and ```null``` while the ```toString()``` can not.**

```js
> String(20)
= '20'
```

- Using the unary ```+``` operator to coerce strings to numbers

```js
+'1' // returns the number value 1
```

- Coercing values to strings with the ```toString()``` method
```js
let number = 123;
console.log(number.toString()); // returns the string "123"
```
This can also be used on arrays:
```js
[1, 2, 3].toString(); // returns the concatenated string "1, 2, 3";
```

## Implicit Coercion

- Using the ```==``` operator

The non-strict equality operator will coerce values that are not of the same type:

1. When a number is compared with a string using ==, the string is coerced into a number.
2. When a boolean is compared with any other value, it is coerced into a number and compared again using the == operator.
3. When an object is compared with a primitive value, the object is coerced into a primitive value and compared again using the == operator.
4. A == comparison of undefined with null evaluates as true.

** When using the non-strict equality operator on two objects, it only returns true if they are the same object.**

- Using the binary ```+``` operator

When one of the operands is a string, the ```+``` operator will coerce the other operand to a string and concatenate them.
```js
console.log('number ' + 1); // returns the string 'number 1'
```

When one of the operands is an object, both are converted to strings and concatenated:
```js
[1] + 2;        // "12"
[1] + '2';      // "12"
[1, 2] + 3;     // "1,23"
[] + 5;         // "5"
[] + true;      // "true"
42 + {};        // "42[object Object]"
```


