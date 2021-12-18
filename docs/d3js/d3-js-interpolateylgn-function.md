# D3.js 插值 lGn()函数

> 原文:[https://www . geesforgeks . org/D3-js-插值 lgn-function/](https://www.geeksforgeeks.org/d3-js-interpolateylgn-function/)

D3.js 中的 **d3 .插值 lGn()** 函数用于从 YlGn 顺序配色方案中返回特定的颜色，该配色方案以 RGB 字符串的形式返回。

**语法:**

```
d3.interpolateYlGn(t)

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **t:**“t”是一个在[0，1]范围内的数字

**返回值:**返回一个 RGB 字符串。

下面是上面给出的函数的几个例子。

**示例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta
            name="viewport"
            path1tent="width=device-width, 
                       initial-scale=1.0"/>
        <title>D3.js interpolateYlGn() Function</title>
    </head>
    <style></style>
    <body>
        <script src=
"https://d3js.org/d3.v4.min.js">
        </script>
        <script src=
"https://d3js.org/d3-color.v1.min.js">
        </script>
        <script src=
"https://d3js.org/d3-interpolate.v1.min.js">
        </script>
        <script src=
"https://d3js.org/d3-scale-chromatic.v1.min.js">
        </script>

        <script>
            console.log(d3.interpolateYlGn(0));
            console.log(d3.interpolateYlGn(0.1));
            console.log(d3.interpolateYlGn(0.001));
            console.log(d3.interpolateYlGn(0.2));
            console.log(d3.interpolateYlGn(0.211));
            console.log(d3.interpolateYlGn(0.3));
            console.log(d3.interpolateYlGn(1));
        </script>
    </body>
</html>
```

**输出:**

![](img/e58bda1312ffb51ca39594ea10b82b5c.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="UTF-8" />
        <meta
            name="viewport"
            content="width=device-width, 
                     initial-scale=1.0"/>
        <title>Document</title>
    </head>
    <style>
        div {
            padding: 10px;
            width: fit-content;
            height: 100px;
        }
    </style>
    <body>
        D3.interpolateYlGn()
        <div class="b1">
            <span>
                D3.interpolateYlGn(0.9)
            </span>
        </div>
        <div class="b2">
            <span>
                D3.interpolateYlGn(0.1)
            </span>
        </div>
        <!--Fetching from CDN of D3.js -->
        <script src=
"https://d3js.org/d3.v4.min.js">
        </script>
        <script src=
"https://d3js.org/d3-color.v1.min.js">
        </script>
        <script src=
"https://d3js.org/d3-interpolate.v1.min.js">
        </script>
        <script src=
"https://d3js.org/d3-scale-chromatic.v1.min.js">
        </script>
        <script>
            // Array of colors is given
            let color1 = d3.interpolateYlGn(0.9);

            let color2 = d3.interpolateYlGn(0.2);

            let b1 = document.querySelector(".b1");
            let b2 = document.querySelector(".b2");
            b1.style.backgroundColor = color1;
            b2.style.backgroundColor = color2;
        </script>
    </body>
</html>
```

**输出:**

![](img/f533a136c00d36b039059dd6db7bf75b.png)