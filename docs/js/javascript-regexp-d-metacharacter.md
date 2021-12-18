# JavaScript | RegExp \d 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-d-meta character/](https://www.geeksforgeeks.org/javascript-regexp-d-metacharacter/)

JavaScript 中的**正则表达式\d 元字符**用于搜索数字字符。与[0-9]相同。

**语法:**

```
/\d/ 
```

或者

```
new RegExp("\\d")
```

**带修饰符的语法:**

```
/\d/g 
```

或者

```
new RegExp("\\d", "g")
```

**示例 1:** 本示例搜索整个字符串中的数字。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \d Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \d Metacharacter</h2>

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
            var regex4 = /\d/g;
            var match4 = str1.match(regex4);

            document.getElementById("app").innerHTML = 
                        "Found " + match4.length
                        + " matches: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backd](img/1c9aa9c16ce9ee47a8ff6d9163daf378.png)
**点击按钮后:**
![backd](img/f8858e108463bb297cbb25ed947eec31.png)

**示例 2:** 本示例搜索整个字符串中的数字。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \d Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \d Metacharacter</h2>

    <p>Input String: Geeky@128</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "Geeky@128";
            var regex4 = new RegExp("\\d", "g");         
            var match4 = str1.match(regex4);

            document.getElementById("app").innerHTML =
                        "Found " + match4.length
                        + " matches: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backd](img/b452e42986ffb2a4bb84626bb3cb1688.png)
**点击按钮后:**
![backd](img/353a5de4a4b6eeb68873d5f0a573f31c.png)

**支持的浏览器:**下面列出了 **RegExp \d 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器