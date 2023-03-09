---
id: xfj1cw13flf2irwhxy4kz97
title: Objects
desc: ''
updated: 1676390535711
created: 1670276925220
---
## Objects in JavaScript

Objects can be a dictionary-like structure with keys matching unique values, i.e.: A key-value pair.

Object literals are created with curly braces, {} , and keys separated from values with a colon, : Mutiple key-value pairs are comma separated:
```js
> { dog: 'barks', cat: 'meows', pig: 'oinks' }
= { dog: 'barks', cat: 'meows', pig: 'oinks' }
```

Values can be retrieved by their keys:
```js
> ({ dog: 'barks', cat: 'meows', pig: 'oinks' })['cat']
= 'meows'
// or objects variable name and key in brackets
// animals['cat'];
```