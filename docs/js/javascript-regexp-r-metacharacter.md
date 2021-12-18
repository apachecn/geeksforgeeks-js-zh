# JavaScript | RegExp \r 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-r-meta character/](https://www.geeksforgeeks.org/javascript-regexp-r-metacharacter/)

JavaScript 中的 **RegExp \r 元字符**用于查找回车符(回车表示返回当前行的开头，不向下前进)。如果找到，它返回位置，否则返回-1。

**语法:**

```
/\r/ 
```

或者

```
new RegExp("\\r")
```

**示例 1:** 本示例在字符串中搜索回车符。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \r Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \r Metacharacter</h2>

    <p>Input String: GeeksforGeeks@_123_{content}lt;/p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\r/;
            var match4 = str1.search(regex4);
            if(match4 == -1) {         
                document.getElementById("app").innerHTML
                = "No carriage return character present. ";
            } else {
                document.getElementById("app").innerHTML
                = "Index of carriage return charcter: " + match4;
            }
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backr](img/ba158c8a63533cdedd44c382822f866c.png)
**点击按钮后:**
![backr](img/26a3ec85306a16b87c466fa8cf65ef43.png)

**示例 2:** 本示例搜索回车符在字符串中的位置。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \r Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \r Metacharacter</h2>

    <p>String: 123ge\reky456</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "123ge\reky456";
            var regex4 = new RegExp("\\r");         
            var match4 = str1.search(regex4);

            document.getElementById("app").innerHTML
            = " Index of carriage return character: "
            + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backr](img/3691e83a72b0cdfb6076eb8c4fd70ffc.png)
**点击按钮后:**
![backr](img/1d2262a684022de9d23aa8e223049417.png)

**支持的浏览器:**以下列出了**正则表达式元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器