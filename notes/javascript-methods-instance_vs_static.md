---
id: javascript-methods-instance_vs_static
title: JavaScript Methods Instance_vs_static
desc: ''
updated: 1670725669198
created: 1670725669198
isDir: false
id_imported: kvnm1b4b3zmoguoth5z4ab2
title_imported: Instance_vs_static
desc_imported: ''
updated_imported: 1669769222972
created_imported: 1669767446554
---
## Instance vs Static Methods

Instance methods have ```.prototype.``` in their name.

Instance methods are applied to a value type from the constuctor. Example:

```String.prototype.concat('abc')```

However, there is also a static concat method that can be applied to any string value. Example:

```'The first letters of the alphabet are: '.concat('abc')```

Instance methods are called on an instance of an object.
Static methods are called on the constructor of an object.