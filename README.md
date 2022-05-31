# NODEJS_Intro

## Install
공식 홈페이지 : https://nodejs.org/ko/download/
````
// 터미널을 통하여 설치 확인
node -v
````

## Hello World
```Javascript
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
**> node index.js** 로 실행

## module
**모듈**이라는 개념은 노드로 개발한 애플리케이션을 이루는 기본 조각이다.


## npm

## package.json

## express

## router
