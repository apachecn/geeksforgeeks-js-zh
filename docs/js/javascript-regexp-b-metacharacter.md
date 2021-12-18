# JavaScript | RegExp \b 元字符

> 原文:[https://www . geeksforgeeks . org/JavaScript-regexp-B- metachar charter/](https://www.geeksforgeeks.org/javascript-regexp-b-metacharacter/)

JavaScript 中的 **RegExp \b 元字符**用于在单词的开头或结尾查找匹配项。如果找到匹配，则返回单词否则返回空值。

**语法:**

```
/\b/ 
```

或者

```
new RegExp("\\b")
```

**带修饰符的语法:**

```
/\b/g 
```

或者

```
new RegExp("\\b", "g")
```

**示例 1:** 此示例匹配字符串开头的单词“GeeksforGeeks”。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \b Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \b Metacharacter</h2>

    <p>Input String: GeeksforGeeks@_123_{content}lt;/p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeks@_123_{content}quot;;
            var regex4 = /\bgeeksforgeeks/gi;
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
![backd](img/fc99886eb555be945be7426f4ea8756d.png)
**点击按钮后:**
![backd](img/1b14e526785b2fad6314d6d3c74d3847.png)

**示例 2:** 本示例匹配开头的单词“Geeky”，并将其替换为单词“GFG”。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp \b Metacharacter
    </title>
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp \b Metacharacter</h2>

    <p>String: Geeky@128</p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "Geeky@128"; 
            var regex4 = new RegExp("\\bGeeky", "gi");         
            var replace = "GFG";
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
![backd](img/20e9b6b0be6b6c79f04f017f38bc8f1a.png)
**点击按钮后:**
![backd](img/fa1132693dafe1790bce5f04b44773d6.png)

**支持的浏览器:**以下列出了 **RegExp \b 元字符**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器