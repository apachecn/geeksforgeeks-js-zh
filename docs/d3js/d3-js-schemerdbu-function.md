# D3.js schemeRdBu【】功能

> 原文:[https://www.geeksforgeeks.org/d3-js-schemerdbu-function/](https://www.geeksforgeeks.org/d3-js-schemerdbu-function/)

d3.js 中的 **d3.schemeRdBu[]** 函数用于返回十六进制代码中的一种颜色。该方案是 D3.js 中发散配色方案的一部分。这给出了红色和蓝色十六进制代码颜色范围内的颜色。

**语法:**

```
d3.schemeRdBu[k];

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **t:** 是任意数字或十六进制代码的索引。

**返回值:**返回颜色的十六进制颜色代码。

下面的例子说明了 JavaScript 中的 D3.js schemeRdBu[]函数:

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
        <title>D3.js schemeRdBu[] Function</title>
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
            console.log(d3.schemeRdBu[3][0]);
            console.log(d3.schemeRdBu[3][1]);
            console.log(d3.schemeRdBu[11][0]);
            console.log(d3.schemeRdBu[11][1]);
            console.log(d3.schemeRdBu[11][2]);
            console.log(d3.schemeRdBu[11][3]);
        </script>
    </body>
</html>
```

**输出:**

![](img/26fd60eec2c2dbed8e0693e0d302628b.png)

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
        <title>D3.js schemeRdBu[] Function</title>
    </head>
    <style>
        div {
            padding: 5px;
            text-align: center;
            vertical-align: middle;
            display: flex;
            justify-content: center;
            width: fit-content;
            height: 50px;
            float: left;
        }
    </style>
    <body>
        <h2>D3.schemeRdBu()</h2>
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
        <div class="b6">
            <span>
                (0.6)
            </span>
        </div>
        <div class="b7">
            <span>
                (0.7)
            </span>
        </div>
        <div class="b8">
            <span>
                (0.8)
            </span>
        </div>
        <div class="b9">
            <span>
                (0.9)
            </span>
        </div>
        <div class="b10">
            <span style="color: honeydew;">
                (1.0)
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
            // Creating different colors for 
            // different values in a array
            let color1 = d3.schemeRdBu[3][0];
            let color2 = d3.schemeRdBu[3][1];
            let color3 = d3.schemeRdBu[3][2];
            let color4 = d3.schemeRdBu[4][3];
            let color5 = d3.schemeRdBu[10][5];
            let color6 = d3.schemeRdBu[8][5];
            let color7 = d3.schemeRdBu[10][2];
            let color8 = d3.schemeRdBu[11][5];
            let color9 = d3.schemeRdBu[11][1];
            let color10 = d3.schemeRdBu[11][0];

            // Selecting Div using query selector
            let box1 = document.querySelector(".box1");
            let box2 = document.querySelector(".box2");
            let box3 = document.querySelector(".box3");
            let box4 = document.querySelector(".box4");
            let box5 = document.querySelector(".box5");
            let b6 = document.querySelector(".b6");
            let b7 = document.querySelector(".b7");
            let b8 = document.querySelector(".b8");
            let b9 = document.querySelector(".b9");
            let b10 = document.querySelector(".b10");

            // Setting style and BG color of the particular DIVs
            box1.style.backgroundColor = color1;
            box2.style.backgroundColor = color2;
            box3.style.backgroundColor = color3;
            box4.style.backgroundColor = color4;
            box5.style.backgroundColor = color5;
            b6.style.backgroundColor = color6;
            b7.style.backgroundColor = color7;
            b8.style.backgroundColor = color8;
            b9.style.backgroundColor = color9;
            b10.style.backgroundColor = color10;
        </script>
    </body>
</html>
```

**输出:**

![](img/10c846d204344bfc4c19a67934dc4342.png)