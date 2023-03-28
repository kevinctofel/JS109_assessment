## RegEx

Regular expressions are character sequences to test for matching patterns in strings. The RegEx sequence is placed between two forward slashes. You can store a RegEx in a variable or use a RegEx object. Example using the ```test()``` method on a RegEx object.
```js
> /o/.test('bobcat')
= true

> /l/.test('bobcat')
= false
```
The RegEx ```match()``` method returns an array with all matches, or ```null``` if there is no match.

The ```/g``` flag signifies a global match so the returned array includes all matching substrings.

