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
```Javascript
/* './routes/index' */
const express = require('express'); // require 메서드를 통해 모듈을 가져옴
const router = express.Router();

router.get('/', function(req, res, next) {
  res.render('index', { title: 'Express' });
});

module.exports = router;  // exports를 통해 외부에서 해당 모듈을 사용하도록 허용 (js에서 js 참조 가능)
```

## npm
**npm**은 Node.js에서 사용 가능한 모듈들을 패키지화시켜 모아놓은 것으로, npm이란 이름은 **Node Package Manager**의 약자입니다.
```
npm [명령어] [타겟 모듈 이름] [옵션]
npm install -g npm          // global 설치
npm install express --save  // package.json, package-lock.json 파일에 의존성 정보가 기재
npm update                  // 모듈 업데이트
npm uninstall               // 모듈 삭제
```
## package.json
**package.json** 파일은 배포한 모듈 정보를 담고자 만들어졌다. (의존성 관리)
```
npm init      // package.json 생성
npm install   // dependencies 모듈 설치
```
```json
{
  "name": "node-api-test",
  "version": "0.0.0",
  "private": true,
  "scripts": {
    "start": "node ./bin/www",
    "dev": "nodemon ./bin/www"
  },
  "dependencies": {
    "cookie-parser": "~1.4.4",
    "debug": "~2.6.9",
    "ejs": "~2.6.1",
    "express": "~4.16.1",
    "http-errors": "~1.6.3",
    "morgan": "~1.9.1"
  },
  "devDependencies": {
    "nodemon": "^2.0.16"
  }
}
```
## express

## router
