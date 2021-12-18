# JavaScript | RegExp \W 元字符

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-w-meta character/](https://www.geeksforgeeks.org/javascript-regexp-w-metacharacter/)

JavaScript 中的 **RegExp \W 元字符**用于查找非单词字符，即不是从 A 到 Z、A 到 Z、0 到 9 的字符。这和^a-zA-Z0-9].一样

**语法:**

```
/\W/ 
```

或者

```
new RegExp("\\W")
```

**带修饰符的语法:**

```
/\W/g 
```

或者

```
new RegExp("\\W", "g")
```

**示例 1:** 本示例搜索非单词字符。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \W Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \W Metacharacter</h2>

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
            var regex4 = /\W/g;
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
![backW](img/ec7f78caae828d687ab57ca54dedaef8.png)
**点击按钮后:**
![backW](img/625626904bd5ef359c83679a933b3b54.png)

**示例 2:** 本示例搜索整个字符串中的非单词字符。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \W Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \W Metacharacter</h2>

    <p>Input String: Geeky@128</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "Geeky@128";         
            var regex4 = new RegExp("\\W", "g");
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
![backW](img/6cc65215ac7aedcd581bb8e348f78559.png)
**点击按钮后:**
![backW](img/9b93534c2bad473fde665938d7c08367.png)

**支持的浏览器:**下面列出了 **RegExp \W 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器