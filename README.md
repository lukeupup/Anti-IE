Anti-IE
=======

弹出窗口提示用户升级浏览器

![DEMO](demo.png "DEMO")

# 特性

- 不依赖其他JS库
- 仅需载入js文件，css和图片自动加载

# 使用方法

## 1. 加载github上的文件

如果需要在版本低于8的IE中显示提示，只需在html里面加上：

    <!--[if lt IE 8]>
    <script type="text/javascript" src="http://lukeupup.github.io/Anti-IE/anti-ie.js"></script>
    <![endif]-->
    
优点：懒人做法。一步到位，不需任何改动，不需要把源码拷到本地。

缺点：速度较慢，有被墙或被github阻止的危险。**很可能因为版本更新导致js/css失效**。

## 2. 拷贝源码加到自己的项目中

分别下载anti-ie.js，anti-ie.css，img文件夹下的4张图片到自己的项目里。

如果需要配置css和图片路径，在引入anti-ie.js前，声明全局对象anti_ie_config，并修改其`cssPath`和`imgPath`属性。
请注意，`cssPath`和`imgPath`都是**相对anti-ie.js的路径**。请注意在路径最后需要加斜杠。
因为在js代码中会引用css和图片文件，因此**请不要修改文件名**。

    <!--[if lt IE 8]>
    <script type="text/javascript">
      var anti_ie_config = {
        cssPath: '../css/'
        imgPath: '../img/anti-ie/'
      };
    </script>
    <script type="text/javascript" src="anti-ie.js"></script>
    <![endif]-->

# Bug或需求

提交Bug或需求到https://github.com/lukeupup/Anti-IE/issues ，请尽量详细描述。