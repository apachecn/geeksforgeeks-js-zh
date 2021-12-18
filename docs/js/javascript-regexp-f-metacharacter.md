# JavaScript | RegExp \f 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-f-meta character/](https://www.geeksforgeeks.org/javascript-regexp-f-metacharacter/)

JavaScript 中的**正则表达式\f 元字符**用于查找表单提要字符(表单提要是一个分页的 ASCII 控制字符)。如果找到，它返回位置，否则返回-1。

**语法:**

```
/\f/ 
```

或者

```
new RegExp("\\f")
```

**示例 1:** 本示例在字符串中搜索表单提要字符。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \f Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \f Metacharacter</h2>

    <p>Input String: GeeksforGeeks@_123_{content}lt;/p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\f/;
            var match4 = str1.search(regex4);
            if(match4 == -1) {         
                document.getElementById("app").innerHTML
                = "No form feed character present. ";
            } else {
                document.getElementById("app").innerHTML
                = "Index of form feed character: " + match4;
            }
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backf](img/54619e216019d8404846a3fd18e9ccd4.png)
**点击按钮后:**
![backf](img/cc85552d7d45c829cf01ef45cbe559fa.png)

**示例 2:** 本示例搜索表单馈送字符在字符串中的位置。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \f Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \f Metacharacter</h2>

    <p>String: 123ge\feky456</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "123ge\feky456";
            var regex4 = new RegExp("\\f");         
            var match4 = str1.search(regex4);
            document.getElementById("app").innerHTML = 
            " Index of form feed character: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backf](img/484fc2ee00eddc30717a51acc9b55cb7.png)
**点击按钮后:**
![backf](img/84caabe55ceb5d43b02a41c1272496ed.png)

**支持的浏览器:**以下列出了 **RegExp \f 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器