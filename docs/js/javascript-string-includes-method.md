# JavaScript 字符串包含()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-includes-method/](https://www.geeksforgeeks.org/javascript-string-includes-method/)

下面是字符串包含()方法的示例。

**例:**

## java 描述语言

```
<!DOCTYPE html>
<html>
    <body>
        <p id="GFG"></p>

        <script>
            var str = "Welcome to GeeksforGeeks.";
            var check = str.includes("Geeks");
            document.getElementById("GFG").innerHTML = check;
        </script>
    </body>
</html>
```

输出:

```
true
```

在 JavaScript 中，includes()方法确定字符串中是否包含给定的字符。如果字符串包含字符，此方法返回 true，否则返回 false。
**注意:**includes()方法区分大小写，即它会区别对待大写字符和小写字符。
**语法:**

```
string.includes(searchvalue, start)
```

**使用的参数:**

*   **搜索值:**是进行搜索的字符串。
*   **开始:**这是搜索将被处理的位置
    (虽然如果没有提到，这个参数不是必需的，搜索将从字符串的开始开始)。
*   返回布尔值 true 表示存在，或者返回 false 表示不存在。

**例:**

```
Input : Welcome to GeeksforGeeks.
        str.includes("Geeks");

Output : true
```

说明:由于没有定义第二个参数，搜索将从起始索引开始。它将搜索极客，因为它存在于字符串中，它将返回真。

```
Input: Welcome to GeeksforGeeks.

Output: false
```

**说明:**即使在这种情况下也没有定义第二个参数，因此搜索将从起始索引开始。但是由于这个方法区分大小写，所以它会对两个字符串进行不同的处理，从而返回一个布尔值 false。
因为区分大小写。
*<u>上述功能的代码如下。</u>*
**代码 1:**

## java 描述语言

```
<!DOCTYPE html>
<html>
    <body>
        <p id="GFG"></p>

        <script>
            var str = "Welcome to GeeksforGeeks.";
            var check = str.includes("Geeks");
            document.getElementById("GFG").innerHTML = check;
        </script>
    </body>
</html>
```

输出:

```
false
```

**代码 2:**

## java 描述语言

```
<!DOCTYPE html>
<html>
    <body>
        <p id="GFG"></p>

        <script>
            var str = "Welcome to GeeksforGeeks.";
            var check = str.includes("geeks");
            document.getElementById("GFG").innerHTML = check;
        </script>
    </body>
</html>
```

输出:

```
false
```

**代码 3:**

## java 描述语言

```
<!DOCTYPE html>
<html>
    <body>
        <p id="GFG"></p>

        <script>
            var str = "Welcome to GeeksforGeeks.";
            var check = str.includes("o", 17);
            document.getElementById("GFG").innerHTML = check;
        </script>
    </body>
</html>
```

输出:

```
true
```

**代码 4:**

## java 描述语言

```
<!DOCTYPE html>
<html>
    <body>
        <p id="GFG"></p>

        <script>
            var str = "Welcome to GeeksforGeeks.";
            var check = str.includes("o", 18);
            document.getElementById("GFG").innerHTML = check;
        </script>
    </body>
</html>
```

输出:

```
false
```

**例外:**

*   如果第二个参数，即计算的索引(起始索引)大于或等于字符串长度，则不会处理搜索，因此返回 false。

## java 描述语言

```
<!DOCTYPE html>
<html>
    <body>
        <p id="GFG"></p>

        <script>
            var str = "Welcome to GeeksforGeeks.";
            var check = str.includes("o", 25);
            document.getElementById("GFG").innerHTML = check;
        </script>
    </body>
</html>
```

输出:

```
false
```

*   如果计算的索引(起始索引)即搜索开始的位置小于 0，将搜索整个数组。

## java 描述语言

```
<!DOCTYPE html>
<html>
    <body>
        <p id="GFG"></p>

        <script>
            var str = "Welcome to GeeksforGeeks.";
            var check = str.includes("o", -2);
            document.getElementById("GFG").innerHTML = check;
        </script>
    </body>
</html>
```

输出:

```
true
```

**支持的浏览器:**

*   Chrome 41 及以上
*   边缘 12 及以上
*   Firefox 40 及以上版本
*   歌剧 28 及以上
*   Safari 9 及以上

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。