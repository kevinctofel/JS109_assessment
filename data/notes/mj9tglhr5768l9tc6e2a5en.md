## Infinity and -Infinity in JavaScript

Infinity is different from NaN; it's a number that's so large, it can't be represented numerically

Division by zero will return Infinity, except in the case of 0 / 0

-Infinity is an infinate value less than zero.

Infinity's type is Number

You can test for infinity with with strict equality

```js
let value1 = Infinity
value1 === Infinity
true

let value2 = -Infinity
value2 === -Infinity
```