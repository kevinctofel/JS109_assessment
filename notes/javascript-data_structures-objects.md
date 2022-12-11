---
id: javascript-data_structures-objects
title: JavaScript Data_structures Objects
desc: ''
updated: 1670725669197
created: 1670725669197
isDir: false
id_imported: xfj1cw13flf2irwhxy4kz97
title_imported: Objects
desc_imported: ''
updated_imported: 1670277426334
created_imported: 1670276925220
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
// or objecta variable name and key in brackets
// animals['cat'];
```