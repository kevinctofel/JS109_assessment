---
id: javascript-coercion
title: JavaScript Coercion
desc: ''
updated: 1670725669195
created: 1670725669196
isDir: false
id_imported: r5xdkanjp8myc7euvod3v1c
title_imported: Coercion
desc_imported: ''
updated_imported: 1670276528705
created_imported: 1670275182089
---
## Explicit Coercion

If we want to change a data type, such as a string of numbers to a Number type, we perform an explicity type coercion.

- String to Numbers

Use the Number function to coerce a string to a number:
```js
> Number('1')
= 1
```

The Number function accepts a string value argument, returning a number if the string is comprised of valid numeric data. If the string doesn't have valid numeric data, Number() will return NaN

- parseInt() function alternative

Similar to the Number() function for coercion but works with a mix of string data comprised of numbers and non-numeric characters. It will convert string numbers until it reaches an invalid character.
```js
> parseInt('12xyz')
= 12
```
Note that if you pass a fractional character to parseInt() it will only return the integer value, not any decimal values less than 1.
```js
> parseInt('3.1415')
= 3
```

- parseFloat() alternative

However, the parseFloat() function will handle fractional numbers for explicit coercion.
```js
> parseFloat('12.5foo')
= 12.5
```

- Numbers to strings

To explicity coerce numbers into a string data type, use the String() function.

```js
> String(20)
= '20'
```




