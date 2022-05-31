# NODEJS_Intro

## Install
공식 홈페이지 : https://nodejs.org/ko/download/
````
// 터미널을 통하여 설치 확인
node -v
````

## Hello World
````
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
````

## module

## npm

## package.json

## express

## router
