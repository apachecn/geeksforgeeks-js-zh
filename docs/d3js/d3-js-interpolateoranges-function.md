# D3.js 插值函数

> 原文:[https://www . geeksforgeeks . org/D3-js-interpoleoranges-function/](https://www.geeksforgeeks.org/d3-js-interpolateoranges-function/)

d3.js 中的 **d3 .插值 Oranges()** 函数是顺序配色方案的一部分。此函数用于返回与顺序配色方案中的颜色相对应的 RGB 字符串。

**语法:**

```
d3.inteprolateOranges(t);

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **t:** 是 0 到 1 范围内的任意数字。

**返回值:**返回一个 RGB 字符串。

下面的例子说明了 JavaScript 中的 D3.js 插值函数:

**示例 1:**

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
        <title>D3.js interpolateOranges() Function</title>
    </head>
    <style></style>
    <body>
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
            console.log(d3.interpolateOranges(0));
            console.log(d3.interpolateOranges(0.4));
            console.log(d3.interpolateOranges(0.2));
            console.log(d3.interpolateOranges(0.25));
            console.log(d3.interpolateOranges(0.54));
            console.log(d3.interpolateOranges(0.85));
            console.log(d3.interpolateOranges(2));
            console.log(d3.interpolateOranges(1));
        </script>
    </body>
</html>
```

**输出:**

![](img/5ca8407077b9c317b3a167c9015c3e86.png)

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
            padding: 6px;
            text-align: center;
            vertical-align: middle;
            display: flex;
            justify-content: center;
            width: 90px;
            height: 50px;
            float: left;
        }
    </style>
    <body>
        <h2>D3.interpolateOranges()</h2>
        <div class="box1">
            <span>
                (0.1)
            </span>
        </div>
        <div class="box2">
            <span>
                (0.2)
            </span>
        </div>
        <div class="box3">
            <span>
                (0.3)
            </span>
        </div>
        <div class="box4">
            <span>
                (0.4)
            </span>
        </div>
        <div class="box5">
            <span>
                (0.5)
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
            // Creating different colors for different
            // Values of t as 0.1,0.2...
            let color1 = d3.interpolateOranges(0.1);
            let color2 = d3.interpolateOranges(0.2);
            let color3 = d3.interpolateOranges(0.3);
            let color4 = d3.interpolateOranges(0.4);
            let color5 = d3.interpolateOranges(0.5);

            // Selecting Div using query selector
            let box1 = document.querySelector(".box1");
            let box2 = document.querySelector(".box2");
            let box3 = document.querySelector(".box3");
            let box4 = document.querySelector(".box4");
            let box5 = document.querySelector(".box5");

            // Setting style and BG color of the particular DIVs
            box1.style.backgroundColor = color1;
            box2.style.backgroundColor = color2;
            box3.style.backgroundColor = color3;
            box4.style.backgroundColor = color4;
            box5.style.backgroundColor = color5;
        </script>
    </body>
</html>
```

**输出:**

![](img/ef524d635499d50a59dd28ee8b70a7a2.png)