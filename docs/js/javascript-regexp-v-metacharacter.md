# JavaScript | RegExp \v 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-v-meta character/](https://www.geeksforgeeks.org/javascript-regexp-v-metacharacter/)

JavaScript 中的**正则表达式\v 元字符**用于查找垂直制表符。如果找到，它返回位置，否则返回-1。

**语法:**

```
/\v/ 
```

或者

```
new RegExp("\\v")
```

**示例 1:** 本示例搜索字符串中的垂直制表符。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \v Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \v Metacharacter</h2>

    <p>Input String: GeeksforGeeks@_123_{content}lt;/p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\v/;
            var match4 = str1.search(regex4);
            if(match4 == -1) {         
                document.getElementById("app").innerHTML
                = "No vertical tab character present. ";
            } else {
                document.getElementById("app").innerHTML = 
                "Index of vertical tab character: " + match4;
            }
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backv](img/37d5364240cf740689a7f51f166785ca.png)
**点击按钮后:**
![backv](img/2e162253a14f352c3a8688951652a9c7.png)

**示例 2:** 本示例搜索字符串中垂直制表符的位置。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \v Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \v Metacharacter</h2>

    <p>String: 123ge\veky456</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "123ge\veky456";
            var regex4 = new RegExp("\\v");         
            var match4 = str1.search(regex4);
            document.getElementById("app").innerHTML
                = " Index of vertical tab character: "
                + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backv](img/9d6fd12468aff2c6b50d62a6a0ced620.png)
**点击按钮后:**
![backv](img/72740124aba7c5070c4cdfbfd7e88a76.png)

**支持的浏览器:**下面列出了 **RegExp \v 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器