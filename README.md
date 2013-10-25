Anti-IE
=======

弹出窗口提示用户升级浏览器

![DEMO](demo.png "DEMO")

# 特性

- 不依赖其他JS库
- 仅需载入js文件，css和图片自动加载

# 使用方法

    <!--[if lt IE 8]>
    <script type="text/javascript" src="anti-ie.js"></script>
    <![endif]-->
    
如果需要配置css和图片路径，在引入anti-ie.js前，声明全局对象anti_ie_config，并修改其`cssPath`和`imgPath`属性。请注意，`cssPath`和`imgPath`都是**相对anti-ie.js的路径**：

    <!--[if lt IE 8]>
    <script type="text/javascript">
      var anti_ie_config = {
        cssPath: '../css/'
        imgPath: '../img/'
      };
    </script>
    <script type="text/javascript" src="anti-ie.js"></script>
    <![endif]-->