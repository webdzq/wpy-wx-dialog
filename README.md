### 小程序项目
> 本项目的appid=`wxb0173de6992165dc`

#### 项目结构介绍   

> `app.wpy`是启动文件，相当于小程序中的`app文件`,设置全局配置。

> `page` 是页面目录，`components` 是组件目录,`mixins`是混合组件目录，`store`是`redux`文件目录，`iamges` 是图片字体目录 ，`style`是全局样式目录，`util`是工具函数目录，`test`是mock数据目录。

#### 后端接口文档：
> 文档地址：http://ewiki.baijiahulian.com/%E9%AB%98%E9%80%94/%E6%8E%A5%E5%8F%A3%E6%96%87%E6%A1%A3/%E5%B0%8F%E7%A8%8B%E5%BA%8F/7.%20%E7%94%A8%E6%88%B7%E8%AF%BE%E7%A8%8B%E6%8E%A5%E5%8F%A3.md
#### 文件命名规范

> 模块语义化、见名知意、驼峰或下划线命名

#### 开发技术介绍 
> wepyjs 框架：[wepyjs文档](https://tencent.github.io/wepy/document.html)

> vuejs：https://cn.vuejs.org/v2/guide/

> es6:http://es6.ruanyifeng.com/

> redux中文文档：http://www.redux.org.cn/

> 小程序文档：https://mp.weixin.qq.com/debug/wxadoc/dev/component/

> ui使用weui：https://github.com/Tencent/weui-wxss 

> demo 参考官网组件demo和小程序UIdemo：https://mp.weixin.qq.com/debug/wxadoc/dev/demo.html

> weweb小程序转h5/ios/android框架:https://github.com/wdfe/weweb

> mock数据：参见`test`目录中的`test_util.js`和`test_config.js`

> axios应用（暂时不建议用）:https://github.com/hjkcai/wepy-plugin-axios

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

> `.wxs`文件只能引入到`page`页面中，`component`组件不起作用。在页面中可以当做过滤器使用。

> `component`组件中有页面跳转时，url的路径以调用组件的页面路径为准，尽量不要在页面中使用路径相关的文件。

> `component`和`page`交互方式多种：props和events都可以传递初始化数据和发送事件数据。


