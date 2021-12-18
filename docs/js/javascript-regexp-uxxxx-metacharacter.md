# JavaScript | RegExp \ uxxx 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-uxxx-meta character/](https://www.geeksforgeeks.org/javascript-regexp-uxxxx-metacharacter/)

JavaScript 中的**RegExp \ uxxx 元字符**用于查找十六进制数 xxxx 指定的 unicode 字符。如果找到匹配，则返回单词否则返回空值。

**语法:**

```
/\uxxxx/ 
```

或者

```
new RegExp("\\uxxxx")
```

**带修饰符的语法:**

```
/\uxxxx/g 
```

或者

```
new RegExp("\\uxxxx", "g")
```

**示例 1:** 本示例匹配整个字符串中对应于十六进制数 0047 即 G 的单词。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \uxxxx Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \uxxxx Metacharacter</h2>

    <p>Input String: GeeksforGeeks@_123_{content}lt;/p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\u0047/gi;
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
![hexax](img/8dfcfb5a268e434b3b2f62799b4c0b37.png)
**点击按钮后:**
![hexax](img/e5d0c9a2847849893723a6f620f28032.png)

**例 2:** 本例匹配对应于“G”的十六进制数(0067)，并用“G”替换。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \uxxxx Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \uxxxx Metacharacter</h2>

    <p>String: geeky@128</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "geeky@128";
            var regex4 = new RegExp("\\u0067", "gi");         
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
![hexax](img/1b8ef019807adee519ae1147ba3123c4.png)
**点击按钮后:**
![hexax](img/d638eafda77e3056a758bf43983b17fb.png)

**支持的浏览器:**下面列出了**RegExp \ uxxx 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器