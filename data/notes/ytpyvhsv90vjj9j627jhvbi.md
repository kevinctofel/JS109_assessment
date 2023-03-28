## Exceptions

Exceptions are errors thrown by JavaScript, which halt the program. To continue the program, a ```catch``` statement can be used:
```js
try {
  // perform an operation that may produce an error
} catch (exception) {
  // an error occurred. do something about it.
  // for example, log the error
} finally {
  // Optional 'finally' block; not used often
  // Executes regardless of whether an exception occurs.
}
```

### Syntax error
These occur as soon as JavaScript program is loaded and before it runs.