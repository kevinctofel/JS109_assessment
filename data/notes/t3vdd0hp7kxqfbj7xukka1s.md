
## Functions have side effects in these instances

1. When a function reassigns a non-local (or outside of function scope) variable.
2. When a function mutates an object value referenced by a non-local variable.
3. When reading or writing to a file, network connection, browser or the console.
4. When a function raises an exception without handling the exception.
5. When a function calls another function that has side effects.

**Functions should return a useful value OR have a side effect, but not BOTH.**

