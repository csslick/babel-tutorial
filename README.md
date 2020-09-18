# babel-tutorial
1. node.js 설치   
<br/>

2. 프로젝트 폴더 생성 후 ```npm init -y```  
<br/>

3. Babel JavaScript compiler 홈페이지 https://babeljs.io/ 을 통해 babel 설치
```
npm install --save-dev @babel/core @babel/cli
```
package.json에 해당 Dependency들이 설치 되었는지 확인
```
{
  "devDependencies": {
    "@babel/cli": "^7.0.0",
    "@babel/core": "^7.0.0"
  }
}
```
<br/>

3.프로젝트 폴더에 ```index.html```과 ```src```(자바스크립트 소스폴더), ```js```(자바스크립트가 빌드될 폴더)를 각각 만든다.
<br/>
<br/>

4. package.json 수정
```
  "scripts": {
    "build": "babel src -d js -w"
  },
```
babel 뒤에 옵션: ```src```는 소스 경로, ```-d 빌드될 소스경로``` ```-w``` watch(실시간 코드 수정)
```index.html```에서는 ```js/main.js```로 파일명(빌드 과정에서 생성됨)을 연결하고 직접 작성할 소스는 ```src```에 같은 이름으로 만든다.
<br/><br/>


5. ```.babelrc``` 설정 파일을 root에 추가하고 관련 모듈을 설치
```npm install @babel/preset-env --save-dev``` 

```babelrc```파일에 다음의 설정을 추가

```
{
  "presets": ["@babel/preset-env"]
}
```
<br/>


6. package.json 수정
``` npm run build ``` 를 실행하면 ```src```의 자바스크립트 파일이 컴파일 되어 ```js```에 저장이 된다.


