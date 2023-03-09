---
id: 9lyni3i9dgfmj513bytdwsk
title: Methods
desc: ''
updated: 1678120744313
created: 1678119220504
---

### Method Chaining
Example: 
```js
let str = 'Pete Hanson';
let names = str.toUpperCase().split(' ').reverse().join(', ');
console.log(names); // => HANSON, PETE
```
Note the multiple methods chained together where methods are called on the return value of other methods.