# 建置差異性分析

## Please pick a preset

> 選擇快速建置專案選項

- Default ([Vue 3] babel, eslint)：
- Default ([Vue 2] babel, eslint)
- Manually select features: 自行選擇專案套件與功能

## Check the features needed for your project

> 選擇專案功能

## Choose a version of Vue.js that you want to start the project with

> 選擇 Vue.js 的版本

## Where do you prefer placing config for Babel, ESLint, etc.?

> 選擇 config 檔案的配置

- In dedicated config files：分別放置於不同檔案
- In package.json：都放在 `package.json` 內

## Save this as a preset for future projects?

> 是否將此操作作為將來專案的操作設定

- yes
- no

## Use history mode for router? (Requires proper server setup for index fallback in production)

> 是否對於 router 使用歷程模式

- yes
```javascript=
// router/index.js
const router = createRouter({
    history: createWebHashHistory(process.env.BASE_URL),
    routes
})
```
- no
```javascript=
// router/index.js
const router = createRouter({
    history: createWebHashHistory(),
    routes
})
```

## 基本配置

- node_modules: 所有支援版控的套件
- public: 網頁畫面，在進行 npm run serve 的時候會去啟動的網頁
- src: vue 主要專案編輯的地方
  - assets: 靜態資料，網頁logo、畫面元素圖...等等
  - components: 組件
  - router: 路徑
  - store: vuex 狀態管理
  - views: 畫面
  - App.vue:  main 建立 vue 應用程式目標
  - main: 建立 vue 應用程式與增加套件的地方
- jsconfig.json
- package.json
- package-lock.json

## 額外配置

- vue.config.js: 
- babel.config.js: 
- .browserslistrc: 

## 開發套件 (devDependencies)

### Babel
[Babel官網](https://babel.docschina.org/)
> 解釋
```
Babel 的用處在於當瀏覽器與用戶的中介，Babel 可以規避瀏覽器不支持的 JavaScript 寫法，確保 JavaScript 兼容所有的瀏覽器 => `跨瀏覽器設定`
```

> dependencies
```
core-js: ^3.8.3
```
> devDependencies
```
@babel/core: ^7.12.16
@babel/eslint-parser: ^7.12.16
@vue/cli-plugin-babel: ~5.0.0
```

Babel 會附帶一個 Core-js 的套件

vue.config.js 中有個設定，默認 False，表示 Babel 會將 node_module 中有用到的套件，轉譯成瀏覽器支援的 JavaScript
```javascript=
transpileDependencies: true
```

### ESLint
> 解釋
```
ESLint 可以依設定，來幫忙除錯 JavsScript 文法錯誤
```
> devDependencies
```
@babel/eslint-parser: ^7.12.16
@vue/cli-plugin-eslint: ~5.0.0
eslint: ^7.32.0 
eslint-plugin-vue: ^8.0.3
```
[ESLint](https://eslint.org/)

## 其他 **待研究**
### 額外啟動專案方式
create-vue：一種基於 [Vite](https://vitejs.dev/) 的 `Vue` 專案建立方式

### typescript vs javascript

### tests 測試專案(e2e, unit)

### scss vs css

### 【額外套件】element-ui

安裝:
```shell=
npm install element-ui -S
```