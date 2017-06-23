# Tooltips

简单简洁的信息提示框，支持移动端。

### Demo 预览 
http://demo.webjyh.com/tooltips

![http://webjyh.qiniudn.com/tooltips_qrcode.png](http://webjyh.qiniudn.com/tooltips_qrcode.png)

### 源码说明
1. `./src/` 为源码目录
2. `./dist/` 为打包后输出目录
3. 请使用 dist 目录下的 `css` 和 `js`

### 源码打包
``` bash
# install dependencies
npm install

# build for production with minification
npm run build
``` 

### 组件说明
1. 组件依赖 jQuery 或 Zepto 库
2. 兼容性  `IE10+`, `Google Chrome`, `Firefox`, `Safari`, `Android 4.4+`, `iOS 8.0+` 
3. 因只是个人项目生产中，无意想到要用，所以匆忙写的，功能较单一，可能会遇到意想不到的 Bug。

### 如何使用
```html
<!-- css -->
<link rel="stylesheet" type="text/css" href="tooltips.css"/>

<!-- jQuery || Zepto -->
<script type="text/javascript" src="zepto.js"></script>

<!-- js -->
<script type="text/javascript" src="tooltips.js"></script>

<!-- tooltips -->
<script type="text/javascript">
  $.tooltips('Tooltips !!!');
</script>
```

### API
```javascript
// 直接调用
$.tooltips('Tooltips !!!');

// 设置消失时间
$.tooltips('Tooltips !!!', 5000);

// 配置 options
$.tooltips('Tooltips !!!', {
  type: 'danger',
  duration: 3000,
  callback: function() {
    alert(1);
  }
});
```

### options  说明
参数名  | 默认值 | 类型 | 参数说明
------- | ------ | ---- | --------
type |  `success` | {String} | 提示框的类型，可填写参数 `default`, `success`, `warning`, `danger`
duration | `3000` | {Number} | 设置提示框消失时间，默认 `3000` 毫秒
callback | `function()` | {Function} | 提示框关闭时所调用的回调法。

### 关于 Demo 提示框中的 `icon`
Demo 中带 `icon` 的提示框均是使用 字体图标加样式完成，图标来自 `iconfont`，具体可查看 Demo 源码
