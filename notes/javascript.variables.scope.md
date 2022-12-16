---
id: 7sv6nsm7mek2rulnozsg5ba
title: Scope
desc: ''
updated: 1671214093931
created: 1671213692111
---
## Variable scope in JavaScript

Scope determines where variables and their data are available to a program. 

Block scope: ```let``` and ```const``` variables are accessible in the block they are declared. Blocks are defined by curly braces in JavaScript. These two variable types have the same scope.

Code from one block cannot directly access variables declared in another block as those are out of scope.

Technically, not all code between curly braces is in a block. Object literals, for example do not define a block. Examples:
```js
{
  // this is a block
  let foo = 42;
  console.log(foo);
}

function foo() {
  // not technically a block. However, we can treat it as a block.
  let foo = 42;               // foo has block scope
  console.log(foo);
}

let foo = {
  // this is not a block
  bar: 42,
};
```

Due to block scope, this code returns an error as the variable ```a``` doesn't exist outside of the code block:
```js
if (1 === 1) {
  let a = 'foo';
}

console.log(a); // ReferenceError: a is not defined
```
