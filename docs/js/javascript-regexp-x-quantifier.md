# JavaScript | RegExp {X，}量化

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-regexp-x-quantizer/

JavaScript 中的 **RegExp m{X，}量词**用于查找包含 m 序列的任何字符串的匹配，至少 X 次，其中 X 是一个数字。

**语法:**

```
/m{X, }/ 
```

或者

```
new RegExp("m{X, }")
```

**带修饰符的语法:**

```
/\m{X, }/g 
```

或者

```
new RegExp("m{X, }", "g")
```

**示例 1:** 本示例在整个字符串中至少匹配字符“e”1 次。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp {X,} Quantifier
    </title>
</head>    

<body style="text-align:center">

    <h1 style="color:green">GeeksforGeeks</h1>

    <h2>RegExp {X,} Quantifier</h2>

    <p>Input String: GeeksforGeeeks e@_123_{content}lt;/p>

    <button onclick="geek()">Click it!</button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "GeeksforGeeeks e@_123_{content}quot;;
            var regex4 = /e{1,}/gi;
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
![atleastX](img/0f6f54f11f9beabc61d6877acf202375.png)
**点击按钮后:**
![atleastX](img/19368b7d5a878eca566a09bde6a0481d.png)

**示例 2:** 本示例将包含至少 2 个“e”的单词替换为“{ content }”；性格。

```
<!DOCTYPE html>
<html>

<head>
    <title>
        JavaScript RegExp {X,} Quantifier
    </title>
</head>    

<body style="text-align:center">

    <h1 style="color:green">GeeksforGeeks</h1>

    <h2>RegExp {X,} Quantifier</h2>

    <p>String: ee@128GeeeeK</p>

    <button onclick="geek()">Click it!</button>

    <p id="app"></p>

    <script>
        function geek() {
            var str1 = "ee@128GeeeeK";
            var regex4 = new RegExp("e{2,}", "gi");         
            var replace = "{content}quot;;
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
![atleastX](img/1a7d453795939c923e37945f15b4d8be.png)
**点击按钮后:**
![atleastX](img/1059046fa9b5d01e4ffafdfab4ce3463.png)

**支持的浏览器:**下面列出了 **RegExp {X，}量词**支持的浏览器:

*   谷歌 Chrome
*   苹果 Safari
*   Mozilla Firefox
*   歌剧
*   微软公司出品的 web 浏览器