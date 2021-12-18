# JavaScript | RegExp [abc]表达式

> 原文:[https://www . geesforgeks . org/JavaScript-regexp-ABC-expression/](https://www.geeksforgeeks.org/javascript-regexp-abc-expression/)

JavaScript 中的**正则表达式【abc】表达式**用于搜索括号之间的任何字符。括号内的字符可以是单个字符或一系列字符。

*   **【A-Z】:**用于匹配从大写 A 到 Z 的任意字符
*   **【a-z】:**用于匹配从小写 a 到 z 的任意字符。
*   **【A-z】:**用于匹配从大写 A 到小写 z 的任意字符。
*   **【ABC…】:**用于匹配括号之间的任意字符。

**语法:**

```
/[abc]/ 
```

或者

```
new RegExp("[abc]")
```

**带修饰符的语法:**

```
/\[abc]/g 
```

或者

```
new RegExp("[abc]", "g")
```

**示例 1:** 本示例在整个字符串中搜索[A-G]之间的字符，即大写的 A 到大写的 G。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp [abc] Expression
    </title>    
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp [abc] Expression</h2>

    <p>
        GEEKSFORGEEKS is the computer
        science portal for geeks.
    </p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GEEKSFORGEEKS is the computer"
                        + " science portal for geeks.";
            var regex4 = /[A-G]/g;
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

*   **点击按钮前:**
    ![abc](img/b822037b1283f76e77ba64b2bfbad1c6.png)
*   **点击按钮后:**
    ![abc](img/2e80f250887cd8cf17cc7ebb40cb2a4d.png)

**示例 2:** 本示例搜索整个字符串中[a-g]之间的字符，即小写 a 到小写 g。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp [abc] Expression
    </title>    
</head>

<body style="text-align:center">

    <h1 style="color:green">
        GeeksforGeeks
    </h1>

    <h2>RegExp [abc] Expression</h2>

    <p>
        GEEKSFORGEEKS is the computer
        science portal for geeks.
    </p>

    <button onclick="geek()">
        Click it!
    </button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GEEKSFORGEEKS is the computer"
                       + " science portal for geeks.";
            var regex4 = /[a-g]/g;
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

*   **点击按钮前:**
    ![abc](img/c8ac81aa0552fe43a2cf86516c0cc08d.png)
*   **点击按钮后:**
    ![abc](img/05eadfe6a2bdddc0de5e8f16643f6283.png)

**支持的浏览器:**下面列出了**正则表达式【abc】支持的浏览器:**

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器