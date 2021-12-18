# D3.js stackOrderNone()方法

> 原文:[https://www.geeksforgeeks.org/d3-js-stackordernone-method/](https://www.geeksforgeeks.org/d3-js-stackordernone-method/)

**D3 . stackordernone()方法** o 根据 stack.keys()方法定义的键顺序对序列进行排序。

**语法:**

```
d3.stackOrderNone(series)

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **系列:**这是基于要订购的钥匙的订购的系列。

**返回值:**此方法不返回值。

**示例:**使用 d3.stackOrderNone()函数对堆栈进行排序。

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <meta charset="utf-8">

    <script src=
        "https://d3js.org/d3.v5.min.js">
    </script>
</head>

<body>
    <h1 style="text-align:center; color:green;">
        GeeksforGeeks
    </h1>

    <center>
        <canvas id="gfg" width="200" height="200">
        </canvas>
    </center>

    <script>
        var data = [
            { letter: { a: 3840, b: 1920, c: 960, d: 400 } },
            { letter: { a: 1600, b: 1440, c: 960, d: 400 } },
            { letter: { a: 640, b: 960, c: 640, d: 400 } },
            { letter: { a: 320, b: 480, c: 640, d: 400 } }
        ];

        var stackGen = d3.stack()
            // Defining keys
            .keys(["a", "b", "c", "d"])
            // Ordering
            .order(d3.stackOrderNone);

        var stack = stackGen(data);

        console.log(stack);
    </script>
</body>

</html>
```

**输出:**

![](img/5ce60b9c1a72be85d25631d3cde1a3c0.png)