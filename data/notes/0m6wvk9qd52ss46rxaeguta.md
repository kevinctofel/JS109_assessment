## Variables in JavaScript

Named area in memory to store data.
Should be descriptive so someone reading code will know exactly what the function does.

Part of the broader term called identifiers:
- Variable names declared by let and var
- Constant names declared by const
- Property names of objects
- Function names
- Function parameters
- Class names

## Variables as Pointers

### Working with primitive values
```js
let count = 1;
count = 2;
```
Above we declare a variable called ```count``` and initialize its value to ```1```. Next we assign the value ```2``` to the variable. 

With most primitive values, the variable points to a particular space in memory, or memory location, where the value of the variable is stored.

### Working with Objects and non-mutating operations
```js
let obj = { a: 1 };
obj = { b: 2 };
```
Above we declare an object with the variable name ```obj``` and assign it the key-value pair of ```a: 1```. Next we assign another key-value pair to the same ```obj``` variable. The object contains a new key-value pairs but the memory location of the object is unchanged. 
![Object stored in memory](assets/images/Screenshot%20from%202023-03-06%2011-22-48.png)

Object variables point to memory locations that then point to the stored the stored values. In other words, the variables point to memory references, not the to the actual values being stored.




