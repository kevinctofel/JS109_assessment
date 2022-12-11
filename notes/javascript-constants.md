---
id: javascript-constants
title: JavaScript Constants
desc: ''
updated: 1670725669197
created: 1670725669197
isDir: false
id_imported: 9xur91vvv3l9nb6zciosjqa
title_imported: Constants
desc_imported: ''
updated_imported: 1670617207055
created_imported: 1670617102205
---
'const' is similar to 'let' but is for constant values that are immutable. They can't be assigned a new value.

```js
const INTEREST_RATE = 0.0783;
INTEREST_RATE = 0.0788; // Uncaught TypeError: Assignment to constant variable.
```

You can't simply declare a constant value; you have to initialize it, or assign, it a value at the same time.