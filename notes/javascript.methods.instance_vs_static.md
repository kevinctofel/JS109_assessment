---
id: kvnm1b4b3zmoguoth5z4ab2
title: Instance_vs_static
desc: ''
updated: 1669769222972
created: 1669767446554
---
## Instance vs Static Methods

Instance methods have ```.prototype.``` in their name.

Instance methods are applied to a value type from the constuctor. Example:

```String.prototype.concat('abc')```

However, there is also a static concat method that can be applied to any string value. Example:

```'The first letters of the alphabet are: '.concat('abc')```

Instance methods are called on an instance of an object.
Static methods are called on the constructor of an object.