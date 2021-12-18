# 如何在 Javascript 中将特殊字符转换成 HTML？

> 原文:[https://www . geesforgeks . org/如何将特殊字符转换为 javascript 中的 html/](https://www.geeksforgeeks.org/how-to-convert-special-characters-to-html-in-javascript/)

在 HTML 中，有许多情况下，浏览器在呈现页面时会感到困惑。在 HTML 中，小于号(< ) means the opening of some tag and if we place an element an after it like *‘a’*或*‘h’*则浏览器将它们分别标识为锚点和标题标签。类似的情况还有一些特殊字符，包括小于、速率(@)、前置和反斜杠等。

**问题示例:**此示例说明了 HTML 文本未转换为特殊格式时导致的问题。

```
<html>
    <head>
    </head>
    <body>
        <div>
        If b<a and a<h then b<h. 
<!-- the browser understands it as anchor tag--> 
       </div>
    </body>
</html>
```

b 部分 **< a 部分**有问题。浏览器将其理解为锚点标签。类似的情况还有 b**T8 h**T4**输出:**

```
If b
```

**解决方法 1:** 一种解决方法是手动将特殊符号放在有问题的相应特殊字符的步调中。但是对于非常重的网站来说，很难画出所有的字符，然后用 HTML 呈现出来。

```
<html>

<head>
</head>

<body>
    <div>
        If b
        < a and ab < h then b < h. 
      <!-- the browser understands it as less than-->
    </div>
</body>

</html>
```

**输出:**

```
If b < a and ab < h then b < h.
```

**基于 javascript 的解决方案**另一种方法是使用 JavaScript 将每个特殊字符转换为各自的 HTML 代码。在脚本中，我们将借助一个正则表达式*”来替换所有的特殊特许状；& #" +字符+"；"的 ASCII 值*。我们对页面上的所有文本应用相同的规则。

```
<html>

<head>
    <script>
        function Encode(string) {
            var i = string.length,
                a = [];

            while (i--) {
                var iC = string[i].charCodeAt();
                if (iC < 65 || iC > 127 || (iC > 90 && iC < 97)) {
                    a[i] = ''&#' + iC + ';';
                } else {
                    a[i] = string[i];
                }
            }
            return a.join('');
        }
    </script>
</head>

<body>
    <script>
        document.write(Encode("If b<a and a<h then b<h"));
    </script>
</body>

</html>
```

**输出:**

```
If b<a and a<h then b<h
```