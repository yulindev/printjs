### printjs 打印使用

##### 注意：需使用ref获取dom节点，若直接通过id或class获取则webpack打包部署后打印内容为空

```js
import Print from '@/utils/print' // 引入
Vue.use(Print) // 注册
```
```html
<template>
	<div ref="print">
		打印内容
		<div class="no-print">不打印内容</div>
	</div>
</template>
```
```js
this.$print(this.$refs.print) // 使用
```
##### 自定义类名
```html
<template>
	<div ref="print">
		打印内容
		<div class="no-print-xxx">不打印内容</div>
	</div>
</template>
```
```js
this.$print(this.$refs.print,{'no-print':'.no-print-xxx'}) // 使用
```
