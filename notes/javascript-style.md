---
id: javascript-style
title: JavaScript Style
desc: ''
updated: 1670725669199
created: 1670725669199
isDir: false
id_imported: zb6vb9hi89482ob4pfxzw6e
title_imported: Style
desc_imported: ''
updated_imported: 1669769490293
created_imported: 1669688231405
---
 
## General style
- Two spaces for tabs with indentation set to spaces.

- Comments:
``` javascript
// represents a single line comment
/* is the start of a multiline comment
** it's common for these in lines within a comment block
*/ ends a multiline comment 
```

- camelCase for general function, method or variable names.
- snake_case or kebab-case for file names.
- SCREAMING_SNAKE_CASE for constants or magic numbers.
- CamelCase (aka: PascalCase) for constructor functions.

## Code blocks using curly braces
- First curly brace on the same line as the function name or conditional expression.
- Closing curly brace after the code block

## Operands
- Use spaces between operands and operators:
```javascript
let sum = x + 5; 
```

## Semicolons
- Used to terminate each logical line of code
- Exceptions: If line ends with a curly brack or a colon
- REPL style omits semicolons

