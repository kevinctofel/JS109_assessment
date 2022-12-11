---
id: tm0bc08i4v42pdt22jlk12x
title: Nodejs
desc: ''
updated: 1669687742445
created: 1669687226671
---

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

