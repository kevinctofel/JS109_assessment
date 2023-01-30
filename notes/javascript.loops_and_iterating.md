---
id: 1ee9kds01i6638da5ub39z2
title: Loops and Iterating
desc: ''
updated: 1675038186540
created: 1673922007182
---
## Loops and Iterating

### ```while``` Loops
Useful when you don't know how many iterations to loop.
While loops execute a code block until some condition is met. 
Example:
```js
let counter = 1;
while (counter <= 1000) {
  console.log(counter);
  counter = counter + 1;
}
```

### Looping Over Arrays With while
Example of iterating through an array of names with a ```while``` loop. While condition checks to see if we've iterated through all of the elements in the array, based on the length of the array. Note the index is incremented through each iteration of the loop.

```js
let names = ['Chris', 'Kevin', 'Naveed', 'Pete', 'Victor'];
let upperNames = [];
let index = 0;

while (index < names.length) {
  let upperCaseName = names[index].toUpperCase();
  upperNames.push(upperCaseName);
  index += 1;
}

console.log(upperNames); // => ['CHRIS', 'KEVIN', 'NAVEED', 'PETE', 'VICTOR']
```

### Using a ```do/while``` loop
Similar to a ```while``` loop but guarantees that it will always run through the loop at least one time. Why? Because the ```while``` condition happens after each loop is executed, not before it.

```js
let answer;
do {
  answer = prompt("Do you want to do that again?");
} while (answer === 'y');
```

### ```for``` loops
Another way to implement a loop by specifying an initialization variable, a condition to evaluate, and an increment or decrement of the loop variable.

Example of the above ```while``` loop rewritten as a ```for``` loop:
```js
let names = ['Chris', 'Kevin', 'Naveed', 'Pete', 'Victor'];
let upperNames = [];

for (let index = 0; index < names.length; index += 1) {
  let upperCaseName = names[index].toUpperCase();
  upperNames.push(upperCaseName);
}

console.log(upperNames); // => ['CHRIS', 'KEVIN', 'NAVEED', 'PETE', 'VICTOR']
```

### Controlling loops with ```continue``` and ```break```



