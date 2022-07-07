# vue2.7 + vite Cli 基础脚手架工程
> 搭建vue2.7+vite脚手架

## 核心
- vue2
- vue2-router
- pinia
- vite
- @vitejs/plugin-vue2 （最新单独支持vue2.7开发的vite插件）

## Install
```
pnpm i
```

## Run
```
npm run dev
```

## Other Intr

- vue2.7是无限接近vue3的语法和基本一致的开发体验
- volar - 可以使用这个开发插件
- css v-vind

## vite for vue2.7 plugin
- @vitejs/plugin-vue2

## 搭建vue2.7+vite脚手架具体过程

### 1 创建基本vue2脚手架，这个默认是基于vite+vue2.6
```js
// 基于这个脚手架改造的
npm init vue@2
```

### 2 去除不必要的包依赖
```json
{
  "dependencies": {
    // "@vue/composition-api": "^1.4.6",
    "pinia": "^2.0.11",
    "vue": "^2.6.14",
    "vue-router": "^3.5.3"
  },
  "devDependencies": {
    "@vitejs/plugin-legacy": "^1.7.1",
    // "@vue/runtime-dom": "^3.2.31",
    // "unplugin-vue2-script-setup": "^0.9.3",
    "vite": "^2.8.4",
    // "vite-plugin-vue2": "^1.9.3",
    // "vue-template-babel-compiler": "^1.2.0",
    // "vue-template-compiler": "^2.6.14"
  }
}
```

### 3 安装 `@vitejs/plugin-vue2`

```sh
pnpm i @vitejs/plugin-vue2 -D
```

## 最后

### 迁移从vue.config.js -> vite.config.js注意事项
- .env文件的开头从VUE_APP_xxx改成VITE_APP_xxx
- process.env改成import.meta.env
- 所有的vue文件都要加后缀
- 建议js改成ts，很多错误会提示

## 涉及的链接
- ![https://www.npmjs.com/package/vue](https://www.npmjs.com/package/vue)
- ![https://github.com/vitejs/vite-plugin-vue2/tree/main/playground](https://github.com/vitejs/vite-plugin-vue2/tree/main/playground)
- ![https://pinia.vuejs.org/](https://pinia.vuejs.org/)
- ![https://github.com/unocss/unocss](https://github.com/unocss/unocss)


