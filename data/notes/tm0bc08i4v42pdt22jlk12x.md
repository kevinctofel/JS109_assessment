
## What is Node.js?

[Node.js](https://nodejs.org/en/) is the runtime environment that lets us run JavaScript outside of the browser.    

Node.js is asynchronous and event driven, which is good for scalable network applications.

Simple Node.js web server:
```javascript
const http = require('http');

const hostname = '127.0.0.1';
const port = 3000;

const server = http.createServer((req, res) => {
  res.statusCode = 200;
  res.setHeader('Content-Type', 'text/plain');
  res.end('Hello World');
});

server.listen(port, hostname, () => {
  console.log(`Server running at http://${hostname}:${port}/`);
});
```


## References
[Node.js download page](https://nodejs.org/en/download/)

