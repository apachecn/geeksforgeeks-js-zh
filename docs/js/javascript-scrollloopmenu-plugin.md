# JavaScript 卷轴选单外挂程式

> 哎哎哎::1230【https://www . geeksforgeeks . org/JavaScript-scroll loopmenu 插件/

在本文中，我们将学习如何使用基于 JavaScript 的**滚动循环菜单**插件来实现*滚动循环菜单*。这是另一种简单的交互式滚动菜单，用于开发网页，以获得良好的视觉效果。

**注意:**请下载工作文件夹中的 JavaScript[**scrolloopmenu**](https://github.com/codrops/ScrollLoopMenu/)插件，并在你的 HTML 代码头部包含所需文件。

> <link href="”https://use.typekit.net/rtr2vsr.css”" rel="”stylesheet”" type="”text/css”/">
> <link href = " CSS/base . CSS " rel = "样式表" type = " text/CSS "/>
> <script src = " js/index . js "></script>

**示例:**以下示例演示了使用 HTML 控件和基于 JavaScript 的**滚动循环菜单**插件的滚动循环菜单。插件的“base.css”文件的“menu”、“menu _ item-inner”、“frame _ _ link”等不同类被附加到 HTML 标记上，如下所示，以获得预期的输出。

```html
<!DOCTYPE html>
<html lang="en" class="no-js">
    <head>
        <meta charset="UTF-8" />
        <meta name="viewport"
              content="width=device-width,
                       initial-scale=1" />
        <title>Scroll Loop Menu Plugin</title>
        <meta name="description"
              content="scroll loop animation." />
        <meta name="keywords" 
              content="Enter keywords in your web page" />
        <link rel="stylesheet"
              href="https://use.typekit.net/rtr2vsr.css" />
        <link rel="stylesheet" 
              type="text/css" 
              href="css/base.css" />
    </head>
    <body>
        <div class="frame">
            <h1 class="frame__title">GFG Scroll Loop Menu</h1>
            <div class="frame__links">
                <a href=
"https://www.geeksforgeeks.org/javascript-tutorial/"
                   class="frame__link">
                    JavaScript
                </a>
                <a href=
"https://www.geeksforgeeks.org/css-tutorials/" c
                   lass="frame__link">
                    CSS
                </a>
            </div>
            <span class="frame__button"
                  aria-hidden="true">
              Close</span>
        </div>
        <nav class="menu">
            <div class="menu__item">
                <a class="menu__item-inner">
                  Algorithms</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Data Structures</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Languages</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Interview Corner</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  GATE</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  ISRO CS</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  UGC NET CS</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  CS Subjects</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Web technologies</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Programming</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Careers</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Internship</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Placement course</a>
            </div>
            <div class="menu__item">
                <a class="menu__item-inner">
                  Geek of the Month</a>
            </div>
        </nav>
        <script src="js/index.js"></script>
    </body>
</html>
```

**Output:**
*   In the beginning:

    ![](img/c635a18197b89a89ae340528c61c589a.png)

*   单击带有链接的“div”时，它会将页面重定向到相应的“href”链接。

    ![](img/acfb6847636d891978de74b4b7f0eb68.png)

*   下图显示了**滚动菜单**插件的滚动菜单功能。

    ![](img/cc2cbc883300b197338170ede65fa5a0.png)