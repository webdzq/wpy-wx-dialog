### 小程序项目-dialog

> -实现dialog的显示和隐藏

> -弹窗调起的时候，下边不可以滚动

> -演示

![演示](https://github.com/webdzq/wpy-wx-dialog/blob/master/dialog.gif)

### 使用

> 参考`index.wpy`

#### 开发技术介绍

> -wepyjs 框架：[wepyjs文档](https://tencent.github.io/wepy/document.html)


#### 项目运行

> 安装`node`，安装`wepy` . `npm install wepy-cli -g`

> 命令行执行 `npm install` 安装依赖包

> 命令行执行 `npm run dev` 编译，产生小程序项目目录 `dist`.开启实时编译。（注：如果同时在`微信开发者工具`-->`设置`-->`编辑设置`中勾选了`文件保存时自动编译小程序`，将可以实时预览，非常方便。）

> 使用`微信开发者工具`-->`添加项目`，项目目录请选择`dist`目录。

> `微信开发者工具`-->`项目`-->`关闭ES6转ES5`。 __ 重要：漏掉此项会运行报错。

> `微信开发者工具`-->`项目`-->`关闭上传代码时样式自动补全`。 __ 重要：某些情况下漏掉此项也会运行报错。

> `微信开发者工具`-->`项目`-->`关闭代码压缩上传`。 __ 重要：开启后，会导致真机`computed`, `props.sync` 等等属性失效。（注：压缩功能可使用WePY提供的build指令代替，详见后文相关介绍以及Demo项目根目录中的`wepy.config.js`和`package.json`文件。）

#### vscode配置

> `首选项`-->`设置`
```
{
    "git.ignoreMissingGitWarning": true,
    "editor.fontSize": 14,
    "files.associations": {
        "*.vue": "vue",
        "*.wpy": "vue",
        "*.wxml": "html",
        "*.wxss": "css",
        "*.wxs": "javascript"
    },
    "emmet.syntaxProfiles": {
        "vue-html": "html",
        "vue": "html"
    },
    "vetur.validation.template": false,
    "editor.tabSize": 2
}
```
> 安装工具插件`wpy-beautify`，`vetur`, `Vue 2 Snippets`,`vscode wxml`,`vscode-wechat`,`WeApp Snippets`等js,html,css相关`格式化`和`自动补全`插件.

#### 常见问题

> `$emit(pickerChange.value)`是错误的，华为手机会报错。改为`$emit(pickerChange-value)`。


