# JavaScript | RegExp \n 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-n-meta character/](https://www.geeksforgeeks.org/javascript-regexp-n-metacharacter/)

JavaScript 中的**正则表达式\n 元字符**用于查找换行符。如果找到了，返回字符的位置，否则返回-1。

**语法:**

```
/\n/ 
```

或者

```
new RegExp("\\n")
```

**示例 1:** 本示例搜索字符串中的换行符。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \n Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \n Metacharacter</h2>

    <p>
        Input String: GeeksforGeeks@_123_$
    </p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\n/;
            var match4 = str1.search(regex4);
            if(match4 == -1) {         
                document.getElementById("app").innerHTML
                    = "No newline characters present. ";
            } 
            else {
                document.getElementById("app").innerHTML
                = "Index of newline character: " + match4;
            }
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backn](img/729b3c87980cb2d5d63a19e9651f610d.png)
**点击按钮后:**
![backn](img/600ccdac39fed83647427062bbefcf01.png)

**示例 2:** 本示例搜索字符串中换行符的位置。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \n Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \n Metacharacter</h2>

    <p>String: 123ge\neky456</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "123ge\neky456";
            var regex4 = new RegExp("\\n");         
            var match4 = str1.search(regex4);
            document.getElementById("app").innerHTML
            = " Index of newline character: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backn](img/5997fdcb0e78f6db28eba62e7209760d.png)
**点击按钮后:**
![backn](img/5854250940680b53c9b5077ddf62692f.png)

**支持的浏览器:**下面列出了**正则表达式\n 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器