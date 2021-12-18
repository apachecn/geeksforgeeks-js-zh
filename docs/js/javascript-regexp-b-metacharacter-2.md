# JavaScript | RegExp \B 元字符

> 原文:[https://www . geeksforgeeks . org/JavaScript-regexp-B- metacharacter-2/](https://www.geeksforgeeks.org/javascript-regexp-b-metacharacter-2/)

JavaScript 中的 **RegExp \B 元字符**用于查找单词开头或结尾不存在的匹配项。如果找到匹配项，则返回单词否则返回空值。

**语法:**

```
/\B/ 
```

或者

```
new RegExp("\\B")
```

**带修饰符的语法:**

```
/\B/g 
```

或者

```
new RegExp("\\B", "g")
```

**示例 1:** 本示例匹配单词开头或结尾不存在的单词“for”。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \B Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \B Metacharacter</h2>

    <p>Input String: GeeksforGeeks@_123_{content}lt;/p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
        var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\Bfor/gi;
            var match4 = str1.match(regex4);

            document.getElementById("app").innerHTML = 
                    "Found " + match4.length
                    + " match: " + match4;
        }
    </script>
</body>

</html>                    
```

**输出:**
**点击按钮前:**
![backd](img/8b5c5b3f85bbc785bebec54c56830a7c.png)
**点击按钮后:**
![backd](img/9442701cb68c473adff1229e0251760f.png)

**示例 2:** 本示例匹配单词“Geeky”，并将其替换为“GEEKY”。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \B Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \B Metacharacter</h2>

    <p>String: 123geeky456</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
        var str1 = "123geeky456";
            var regex4 = new RegExp("\\Bgeeky", "gi");         
            var replace = "GEEKY";
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
![backd](img/ea03c0e290ffb3561cb1eefea81e4482.png)
**点击按钮后:**
![backd](img/93fc9651f1b856e51f0efcac560f6c5c.png)

**支持的浏览器:**以下列出了**正则表达式\B 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器