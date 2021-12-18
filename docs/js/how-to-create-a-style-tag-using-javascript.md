# 如何用 JavaScript 创建样式标签？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 创建样式标签/](https://www.geeksforgeeks.org/how-to-create-a-style-tag-using-javascript/)

document.createElement('style ')方法用于使用 JavaScript 创建样式元素。创建样式元素的步骤如下:

**步骤:**

*   使用以下语法创建样式元素
    **语法:**

```
document.createElement('style');
```

*   应用 CSS 样式。
*   将此样式元素附加到头部元素。
    **语法:**

```
document.getElementsByTagName("head")[0].appendChild(styleElement);
```

**示例 1:** 本示例通过使用 JavaScript 创建样式元素，将< h1 >的颜色更改为绿色。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        Create style tag using JavaScript
    </title>
</head>

<body>
    <h1>GeeksForGeeks</h1>

    <!-- Script to add style element -->
    <script type="text/javascript">

        /* Function to add style element */
        function addStyle(styles) {

            /* Create style document */
            var css = document.createElement('style');
            css.type = 'text/css';

            if (css.styleSheet)
                css.styleSheet.cssText = styles;
            else
                css.appendChild(document.createTextNode(styles));

            /* Append style to the tag name */
            document.getElementsByTagName("head")[0].appendChild(css);
        }

        /* Set the style */
        var styles = 'h1 { color: green }';
        styles += ' body { text-align: center }';

        /* Function call */
        window.onload = function() { addStyle(styles) };
    </script>
</body>

</html>                   
```

**输出:**

![](img/ae653989224e754c11308aab941d8c64.png)

**示例 2:** 本示例通过使用 JavaScript 创建样式元素，将< div >元素的< h1 >文本颜色更改为白色，背景颜色更改为绿色。

## 超文本标记语言

```
<!DOCTYPE html> 
<html> 

<head>
    <title>
        Create style tag using JavaScript
    </title>
</head>

<body> 
    <div id="header">
        <h1>GeeksForGeeks</h1>
    </div>

    <!-- Script to create style tag -->     
    <script type="text/javascript">

        /* Function to add style */
        function addStyle(styles) {

            /* Create style element */
            var css = document.createElement('style');
            css.type = 'text/css';

            if (css.styleSheet)
                css.styleSheet.cssText = styles;
            else
                css.appendChild(document.createTextNode(styles));

            /* Append style to the head element */
            document.getElementsByTagName("head")[0].appendChild(css);
        }

        /* Declare the style element */
        var styles = 'h1 { color: white }';
        styles += ' body { text-align: center }';
        styles += ' #header { height: 50px; background: green }';

        /* Function call */
        window.onload = function() { addStyle(styles) };
    </script>   
</body> 

</html>
```

**输出:**

![](img/298f6bc141b98b2a09f46f4fe5d0c1f5.png)