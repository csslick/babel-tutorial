# babel-tutorial
1. node.js 설치  


2. 프로젝트 폴더 생성 후 ```npm init -y```


3. Babel JavaScript compiler 홈페이지 https://babeljs.io/ 을 통해 babel 설치
```
npm install --save-dev @babel/core @babel/cli
```


4. package.json 수정
```
  "scripts": {
    "build": "babel src -d js -w"
  },
```
brbel 뒤에 옵션: ```src```는 소스 경로, ```-d 빌드될 소스경로``` ```-w``` watch(실시간 코드 수정)


