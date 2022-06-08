<p align="center">
    <img alt="logo" src="https://uviewui.com/common/logo.png" width="120" height="120" style="margin-bottom: 10px;">
</p>
<h3 align="center" style="margin: 30px 0 30px;font-weight: bold;font-size:40px;">uView</h3>
<h3 align="center">多平台快速开发的UI框架</h3>


## 说明

uView UI，是[uni-app](https://uniapp.dcloud.io/)生态优秀的UI框架，全面的组件和便捷的工具会让您信手拈来，如鱼得水


## 安装

```bash
# npm方式安装
npm i uview-ui
```

## 快速上手

1. `main.js`引入uView库
```js
// main.js
import uView from 'uview-ui';
Vue.use(uView);
```

2. `App.vue`引入基础样式(注意style标签需声明scss属性支持)
```css
/* App.vue */
<style lang="scss">
@import "uview-ui/index.scss";
</style>
```

3. `uni.scss`引入全局scss变量文件
```css
/* uni.scss */
@import "uview-ui/theme.scss";
```

4. `pages.json`配置easycom规则(按需引入)

```js
// pages.json
{
	"easycom": {
		// npm安装的方式不需要前面的"@/"，下载安装的方式需要"@/"
		// npm安装方式
		"^u-(.*)": "uview-ui/components/u-$1/u-$1.vue"
		// 下载安装方式
		// "^u-(.*)": "@/uview-ui/components/u-$1/u-$1.vue"
	},
	// 此为本身已有的内容
	"pages": [
		// ......
	]
}
```

请通过[快速上手](https://uviewui.com/components/quickstart.html)了解更详细的内容 

## 使用方法
配置easycom规则后，自动按需引入，无需`import`组件，直接引用即可。

```html
<template>
	<u-button>按钮</u-button>
</template>
```

