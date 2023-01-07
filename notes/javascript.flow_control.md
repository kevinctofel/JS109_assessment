---
id: ra0p20kuodsnuloxagh1cke
title: Flow control
desc: ''
updated: 1673050482177
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