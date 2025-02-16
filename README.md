## 🚀 Webpack Setup Guide

📦 Webpack을 직접 설정하고, 번들링 환경을 구축하는 과정을 기록합니다.

<br/>

### 📌 프로젝트 개요
Webpack을 활용한 모듈 번들링 환경을 직접 구축하는 과정과 설정 방법을 정리했습니다. <br/>
바닐라 JS 환경에서 Webpack을 사용하여 번들링을 수행하고, 추가적으로 Babel, CSS 로더, 이미지 로더 등을 설정하는 방법을 다룹니다.

<br/>

### 📂 프로젝트 구조
```
📦 webpack
 ┣ 📂 dist
 ┃ ┣ 📜 index.html  
 ┃ ┣ 📜 main.js
 ┣ 📂 src
 ┃ ┣ 📜 index.js 
 ┣ 📜 index.js
 ┣ 📜 package.json
 ┣ 📜 webpack.config.js
 ┣ 📜 .gitignore
 ┗ 📜 README.md
```

<br/>

### 🔧 Webpack 설정 과정

1. Webpack 및 필수 패키지 설치

```sh
npm install webpack webpack-cli webpack-dev-server -D
npm install babel-loader @babel/core @babel/preset-env -D
npm install css-loader style-loader -D
npm install file-loader image-webpack-loader -D
npm install html-webpack-plugin mini-css-extract-plugin -D
```

<br/>

2. Webpack 설정 파일 작성 (webpack.config.js)
- entry: 번들링의 시작점 지정
- output: 번들 파일의 위치 및 이름 설정
- module.rules: 로더 설정 (Babel, CSS, 이미지)
- plugins: 플러그인 적용 (HTML 생성, CSS 분리)
- devServer: 개발 서버 설정

<br/>
  
🚀 최적화 및 추가 설정
- 압축 및 최적화: image-webpack-loader, CssMinimizerPlugin 적용
- Code Splitting: SplitChunksPlugin을 활용한 코드 분할
- HtmlWebpackPlugin: 번들링된 스크립트를 자동으로 HTML에 삽입
- BundleAnalyzerPlugin: 번들 크기 및 의존성 시각화
- ProgressPlugin: 빌드 진행률 표시
- MiniCssExtractPlugin: CSS 파일을 별도로 분리하여 최적화
