---
id: ra0p20kuodsnuloxagh1cke
title: Flow control
desc: ''
updated: 1673921653500
created: 1673047707671
---
## Flow Control in JavaScript
How a program branches off to do different things based on inputs, outputs, etc...

### Conditionals
Checking "if" something is or happens changes the path or flow of code.

Simplest method is with ```if``` statements, which can also be followed by ```else``` conditions.

```js
if (x === 3) {                  // If statement
  console.log("x is 3");        // Clause to run
}
```
Note in above example, the curly braces for the code block aren't needed. A single statement or expression doesn't require them but it's good practice.

### Comparisons
Comparisons return the boolean values of ```true``` or ```false``` depending on the condition and the operands.

| Operator | Description
|---|---|
|```===```| Strict equality of value and type ; returns ```true``` if they are the same |
|```!==```| Strict inequality of value and type; returns ```false``` if they are the same|
| ```==``` | Non-strict or loose equality. Attempts to coerce types of one or both operands. Returns ```true``` if values but not type are the same.|
|```!=```| Non-strict or loose inequality. Attempt to coerce types of one or both operands. Returns ```false``` if values are the same, regardless of type.|
| ```<``` | Less than returns ```true``` when left operand value is less than the right operand value|
|```>``` | Greater than returns ```true``` when right operand value is greater than left operand value|
|```<=``` | Less than or equal to returns ```true``` when left operand value is less than or equal to the right operand value|
|```>=```| Greater than or equal to returns ```true``` when the left operand value is greater than or equal to the right operand value|
| ```!```| Logical not operator, negates an operand|
|```&&```| Logical and operator, returns ```true``` only if both operands are true|
|&#124&#124| Logical or operator, returns ```true``` if either operand is true|


### Short circuits
Logical operators use short circuit evaluation so they can re-flow code sooner (or not at all) based on just the first operand.

In an ```&&``` evaluation, if the first operand returns ```false```, the second doesn't have to be evaluated.

In an ```||``` evaluation, if the first operand returns ```true```, the second doesn't have to be evaluated.

### Truthiness
```If``` statements always evaluated to ```true``` or ```false```. But expressions can be evaluated for truthiness by JavaScript coercion, where the expression value is changed to represent true or false.

Examples: 
```js
a = 5
if (a) {
  console.log("how can this be true?");
} else {
  console.log("it is not true");
}

b = 0
if (b) {
  console.log("how can this be true?");
} else {
  console.log("it is not true");
}
```
The first statement is truthy because the value of ```a``` is coerced to ```true```.
The second statement is not truthy, or falsy, because the value of ```b``` is coerced to ```false```.

Why? JavaScript coerces the following values to ```false```:
- false
- The numbers 0, -0, and 0n
- ```''```; an empty string
- undefined
- null
- NaN

All other values are coerced to ```true``` in JavaScript.

With ```&&``` and ```||```, truthy and falsy can still short circuit, returning the value of the last evaluated operand.
Rather than test expressions with these with multiple code lines, use a ternary expression for clarity.
Example:
```js
// Instead of this:
let foo = null;
let bar = 'qux';
let isOk = foo || bar;

// Use a ternary expression like this:
let isOk = (foo || bar) ? true : false;
```

### Operator precedence
From highest to lowest: 
- <=, <, >, >= - Comparison
- ===, !==, ==, != - Equality
- && - Logical AND
- || - Logical OR
Note: expressions in parenthesis take precedence over those that are not.

### The ternary operator
Uses a combination of ```?```, ```:``` after the expression, with the truthy and falsy return values inserted.
Example:
```js
> 1 == 1 ? 'this is true' : 'this is not true'
= 'this is true'

> 1 == 0 ? "this is true" : "this is not true"
= 'this is not true'
```
Why use a ternary expression over an ```if/else``` statement? Because it's a single expression and can be treated as value that can be stored, passed in as an argument, etc...

Ternary expressions should be used to select between two values, not two actions. It's good practice to assign the value of a ternary expression to a variable or passed as an argument.
Example:
```js
let foo = hitchhiker ? 42 : 3.1415;    // Assign result of ?: to a variable
console.log(hitchhiker ? 42 : 3.1415); // Pass result as argument
return hitchhiker ? 42: 3.1415;        // Return result
```

### Switch statements
Similar to an ```if``` statement but compares a single value against multiple values for strict equality. It evaluates the expression to the value in each ```case``` clause. The ```break``` statements effectively short circuit the ```switch``` statement by dropping out when the evaluation is truthy.
Example:
```js
let a = 5;

switch (a) {
  case 5:
    console.log('a is 5');
    break;
  case 6:
    console.log('a is 6');
    break;
  default:
    console.log('a is neither 5, nor 6');
    break;
} // => a is 5
```

```Switch``` statements can fall through multiple values that satisfy strict equality, like an ```||``` operator. 
Example:
```js
let a = 5;

switch (a) {
  case 5:
  case 6:
  case 7:
    // executed if a is 5, 6, or 7
    console.log("a is either 5, 6, or 7");
    break;
  case 8:
  case 9:
    // executed if a is 8 or 9
    console.log('a is 8 or 9');
    break;
  default:
    // executed if a is anything else
    console.log('a is not 5, 6, 7, 8, or 9');
    break;
}
```

