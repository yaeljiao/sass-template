# Sass-template
​	使用Sass进行样式编写能够结构化的管理所有样式文件，从而增强样式文件的可读性、维护性。



## 基本目录结构(7–1 Pattern)



```
styles/
|
|-- base/                     # 包含整个项目最基本的基础样式
|	|-- _reset.scss             # 或者_normalize.scss
|	|-- _typography.scss        # 排版样式
|	|-- _base.scss              # 一些通用的html标签的样式，比如<body/>, <a/>
|   …
|
|-- components/               # 基础组件
|   |-- _buttons.scss         # 按钮
|   |-- _search.scss          # 搜索按钮
|   …
|
|-- helpers/
|   |-- _variables.scss       # Sass Variables
|   |-- _functions.scss       # Sass Functions
|   |-- _mixins.scss          # Sass Mixins
|   …
|
|-- layouts/
|   |-- _header.scss          # Header
|   |-- _footer.scss          # Footer
|   |-- _sidebar.scss         # Sidebar
|   …
|
|-- pages/
|   |– _admin.scss            # admin页面的特殊样式
|   |– _login.scss            # login页面的特殊样式
|   |– _main.scss             # main页面的特殊样式
|   …
|
|– themes/
|   |– _theme.scss            # 默认主题
|   …
|
|-- vendor/                   # 来自第三方的CSS或Sass文件，比如Bootstrap, jQuery
|   |-- _hon-dls.min.scss
|   |-- _loadMask.scss    
|   |-- _react-bootstrap-table.min.css 
|   …
|
`-- main.scss                 # 主Sass文件放在最外层目录下
`-- admin.scss
`-- login.scss
`-- changePwd.scss
`-- resetPwd.scss
```



## 主样式表

​	主样式表应该尽可能的干净整洁，所有样式都通过`@import`进行引用。为了保证可读性，主样式表应该遵循如下的规范：

- 一个`@import`对应一个文件
- 一个`@import`占一行
- 相同文件夹下的两个`@import`之间不空行
- 不同文件夹下的两个`@import`之间要空行
- 省略文件后缀，省略前导的`_`下划线



```scss
@import "helpers/variables";
@import "helpers/mixins";

@import 'vendors/loadMask';
@import 'vendors/bootstrap.min.css';

@import "base/base";
@import "base/typography";

@import "components/button";

@import "layout/header";
@import "layout/footer";

@import "pages/_main";
```





## 参考

[sass-guidelin.es/#architecture](https://sass-guidelin.es/#architecture)

[sass-boilerplate](https://github.com/HugoGiraudel/sass-boilerplate)

