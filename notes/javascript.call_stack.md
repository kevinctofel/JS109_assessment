---
id: tldfi2vg3jdn9sqbxit7suk
title: Call Stack
desc: ''
updated: 1678122144919
created: 1672333424449
---
## The Call Stack in JavaScript

This stack tracks what function is executing and what other functions haven't yet executed. It's an ordered stack (LIFO) of functions as they're invoked or called. The stack is created with stack frames; one frame for each function invocation.

[From the MDN](https://developer.mozilla.org/en-US/docs/Glossary/Call_stack):
- When a script calls a function, the interpreter adds it to the call stack and then starts carrying out the function.
- Any functions that are called by that function are added to the call stack further up, and run where their calls are reached.
- When the current function is finished, the interpreter takes it off the stack and resumes execution where it left off in the last code listing.
- If the stack takes up more space than it was assigned, a "stack overflow" error is thrown.

![](/assets/images/2022-12-29-12-09-33.png)

## Stack Trace

[JavaScript exception errors](./javascript.exceptions.md) return a stack trace, showing the type of error and where it occurred.
Example:
```js
$ node error.js
/Users/wolfy/tmp/x.js:2
  console.log(bar);

ReferenceError: bar is not defined
    at foo (error.js:2:15)
    at Object.<anonymous> (error.js:5:1)
    ...
```
