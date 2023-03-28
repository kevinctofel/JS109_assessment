## Input and output in JavaScript

### Command line output
```console.log()``` provides command line output shown in the Terminal and in the console of a browser's dev tools.

### Command line input
Accepting user input requires a Node.js API called ```readline```. For our purposes, we use a library called ```readlineSync``` [available through NPM](https://www.npmjs.com/package/readline-sync).

How to install readline-sync: 
```js
$ npm install readline-sync --save
npm notice created a lockfile as package-lock.
```

How to use readlineSync:
- Use the ```require``` function to import the readline-sync library.
- Assign that function to a variable for later use.
- Use that variable with the readline-sync methods: ```question()```, ```prompt()```, etc..
```js
let rlSync = require('readline-sync');
let name = rlSync.question("What's your name?\n");
console.log(`Good Morning, ${name}!`);
```
Note that ```question()``` returns string data, so when working with numbers, these must be coerced to the ```Number``` data type.

### Browser input (basic)
Include a JS script in the HTML. In the script, use the ```prompt``` function for a user input popup box. Input can be stored as a variable and used elsewhere in the script.

```js
let name = prompt("What's your name?");
console.log(`Good Morning, ${name}`);
```
This data can be sent to the console via ```console.log()``` or through the ```alert``` function in the browser.
