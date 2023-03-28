---
id: 7sv6nsm7mek2rulnozsg5ba
title: Scope
desc: ''
updated: 1679360078114
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

## Global Scope

Variables in JavaScript with no functions or blocks have global scope. Additionally, any variables existing outside of functions or blocks have global scope.

## Local Scope

Two forms of local scope: Function scope and block scope.

### Function Scope

Variable scope is determined by where it is declared, so if you declare a variable in a function it is available to the entire function. Note that nested functions have nested scope.

1. Outer scope variables can be accessed by the inner scope, i.e.: a global variable can be accessed by a function.

2. Inner scope variables can not be accessed by the outer scope. i.e.: code outside of a function can't directly access variables within that function. Typically JavaScript would return a ```ReferenceError``` as the variable is not defined globally.

3. Peer scopes do not conflict, even with the same variable name. 

4. Nested functions have their own variable scope.

5. Inner scope variables can shadow outer scope variables, i.e.: In cases when inner and outer scope variables have the same name, the inner variable prevents the outer variable from being accessed. Example:
```js
let number = 10; // this 'number' is ignored below

[1, 2, 3].forEach(number => {
  console.log(number);
});
```

### Block Scope

Blocks are defined by statements and expressions within curly braces. The rules for block scope are the same as function scope, but limited to within the code block.
