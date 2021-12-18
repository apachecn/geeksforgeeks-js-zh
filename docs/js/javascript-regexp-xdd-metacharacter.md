# JavaScript | RegExp \xdd 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-xdd-meta character/](https://www.geeksforgeeks.org/javascript-regexp-xdd-metacharacter/)

JavaScript 中的 **RegExp \xdd 元字符**用于查找十六进制数 dd 指定的字符。如果找到匹配，则返回字符，否则返回空值。

**语法:**

```
/\xdd/ 
```

或者

```
new RegExp("\\xdd")
```

**带修饰符的语法:**

```
/\xdd/g 
```

或者

```
new RegExp("\\xdd", "g")
```

**例 1:** 本例匹配对应于十六进制数 47 的单词，即整个字符串中的 G。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \xdd Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \xdd Metacharacter</h2>

    <p>Input String: GeeksforGeeks@_123_{content}lt;/p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\x47/gi;
            var match4 = str1.match(regex4);

            document.getElementById("app").innerHTML
                    = "Found " + match4.length
                    + " match: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![hexax](img/7dcc87d26b3d50dffad5355f054c1eb1.png)
**点击按钮后:**
![hexax](img/251eedfb40505e31904d4b1656ed9a46.png)

**示例 2:** 本示例匹配对应于“G”的十六进制数(67)，并将其替换为“G”。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \xdd Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \xdd Metacharacter</h2>

    <p>String: geeky@128</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "geeky@128";
            var regex4 = new RegExp("\\x67", "gi");         
            var replace = "G";
            var match4 = str1.replace(regex4, replace);
            document.getElementById("app").innerHTML = 
                    " New string: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![hexax](img/971eb1ca7fb2f12d1f619a058138a5ce.png)
**点击按钮后:**
![hexax](img/82d72c356126351039ca1fda8f370864.png)

**支持的浏览器:**下面列出了 **RegExp \xdd 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器