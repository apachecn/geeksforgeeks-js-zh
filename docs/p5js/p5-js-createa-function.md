# p5.js | createA()函数

> 原文:[https://www.geeksforgeeks.org/p5-js-createa-function/](https://www.geeksforgeeks.org/p5-js-createa-function/)

p5.js 中的 createA()函数用于在 DOM(文档对象模型)中创建一个锚点元素，用于创建超链接。这个函数包括 p5.dom 库。在标题部分添加以下语法。

## 超文本标记语言

```
<script src=
"https://cdnjs.cloudflare.com/ajax/libs/p5.js/0.5.11/addons/p5.dom.min.js">
</script>
```

**语法:**

```
createA( href, html, target )
```

**参数:**

*   **href:** 它保存链接的页面 url。
*   **html:** 保存显示文本。
*   **目标:**它持有链接将要打开的目标。

“目标”可以是 **'_blank'** (链接将在新的选项卡中打开)、 **'_self'** (链接将在同一选项卡中打开)等。
**示例:**本示例使用 createA()函数创建 GeeksforGeeks 主页的链接。

## java 描述语言

```
// Create a variable for anchor object
var link;

function setup() {

    // Create a canvas
    createCanvas(400, 200);

    // Set the background-color
    background('green');

    // Create a anchor object using createA() function
    link = createA("https://www.geeksforgeeks.org/",
                       "Go to GeeksforGeeks", "_blank");

    // Position the anchor objects
    link.position(120, 80);   
}
```

**输出:**

![](img/756d53f38a1f7d7eed6a03935dddd2ac.png)

点击链接后，极客博客的主页将在一个新的选项卡中打开。
**参考:**[https://p5js.org/reference/#/p5/createA](https://p5js.org/reference/#/p5/createA)