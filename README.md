# babel-tutorial
## 1. node.js 설치   
<br/><br/>

## 2. 프로젝트 폴더 생성 후 ```npm init -y```  

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
babel 뒤에 옵션: ```src```는 소스 경로, ```-d 빌드될 소스경로``` ```-w``` watch(실시간 코드 수정)

5. ```.babelrc``` 설정 파일을 root에 추가하고 관련 모듈을 설치
```npm install @babel/preset-env --save-dev``` 

- ```babelrc```파일에 다음의 설정을 추가

```
{
  "presets": ["@babel/preset-env"]
}
```
