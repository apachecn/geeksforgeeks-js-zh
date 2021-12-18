# JavaScript | RegExp ^数量词

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-量词-5/](https://www.geeksforgeeks.org/javascript-regexp-quantifier-5/)

JavaScript 中的 **RegExp ^m 量词**用于查找任何在其开头包含 m 的字符串的匹配。

**语法:**

```
/^m/ 
```

或者

```
new RegExp("^m")
```

**带修饰符的语法:**

```
/\^m/g 
```

或者

```
new RegExp("^m", "g")
```

**示例 1:** 该示例匹配字符串开头的单词“Geeks”的存在。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp ^ Quantifier
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">GeeksforGeeks</h1>

    <h2>RegExp ^ Quantifier</h2>

    <p>Input String: Geeksfor123\nGeeks@</p>

    <button onclick="geek()">Click it!</button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "Geeksfor123\nGeeks@";
            var regex4 = /^Geeks/gim;
            var match4 = str1.match(regex4);

            document.getElementById("app").innerHTML
                    = "Found " + match4.length
                    + " matches: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![xpower](img/7513a16a83b440c76eb32623767148d1.png)
**点击按钮后:**
![xpower](img/6c63de651f6f6c8395e9a6e11d84a571.png)

**示例 2:** 本示例将字符“@”替换为“#”。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp ^ Quantifier
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">GeeksforGeeks</h1>

    <h2>RegExp ^ Quantifier</h2>

    <p>String: @128Geek</p>

    <button onclick="geek()">Click it!</button>

    <p id="app"></p>

    <script>
        function geek() {
           var str1 = "@128Geek";
            var regex4 = new RegExp("^@", "gi");            
            var replace = "#";
            var match4 = str1.replace(regex4, replace);
            document.getElementById("app").innerHTML = 
                " New string: " +  match4;
        }
    </script>
</body>

</html>
```

**输出:**
**点击按钮前:**
![xpower](img/1e64e5b56be53a18fa5c55083bdc683b.png)
**点击按钮后:**
![xpower](img/2069bb9e1fed723e67f9c232118b3251.png)

**支持的浏览器:**regexp ^量词支持的浏览器如下:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器