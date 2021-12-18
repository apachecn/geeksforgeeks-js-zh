# D3.js 插值器 Bu()函数

> 原文:[https://www . geesforgeks . org/D3-js-interprederbu-function/](https://www.geeksforgeeks.org/d3-js-interpolaterdbu-function/)

D3.js 中的 **d3 .插值器 Bu()** 函数是从 D3.js 中的 RdBu 发散配色方案返回颜色的发散配色方案的一部分，这里 Rd 可以解释为红色，Bu 可以解释为蓝色。请仔细阅读例子，以便更好地理解。

**语法:**

```
d3.interpolateRdBu(t);

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **t:** 这是一个在[0，1]范围内的数字

**返回值:**上述函数返回一个 RGB 字符串。

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
        <title>D3.js interpolateRdBu () Function</title>
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
            // When t is in range [0,1]
            // Value of t varies as 0.1, 0.2 ....1.0
            // Output is RGB string
            console.log(d3.interpolateRdBu(0));
            console.log(d3.interpolateRdBu(0.1));
            console.log(d3.interpolateRdBu(0.2));
            console.log(d3.interpolateRdBu(0.3));
            console.log(d3.interpolateRdBu(0.4));
            console.log(d3.interpolateRdBu(0.5));
            console.log(d3.interpolateRdBu(0.6));
            console.log(d3.interpolateRdBu(0.7));
            console.log(d3.interpolateRdBu(0.8));
            console.log(d3.interpolateRdBu(0.9));
            console.log(d3.interpolateRdBu(1.0));
        </script>
    </body>
</html>
```

**输出:**

![](img/58ccf881ecffb4704d4e3ea13ada7b1d.png)

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
        <title>D3.js interpolateRdBu () Function</title>
    </head>
    <style>
        div {
            margin: 2px;
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
        <h5>
            D3.interpolateRdBu()
        </h5>
        <br />
        <br />
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
            <span>
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
            // Creating different colors for different
            // Values of t as 0.1,0.2... 1.0
            let color1 = d3.interpolateRdBu(0.1);
            let color2 = d3.interpolateRdBu(0.2);
            let color3 = d3.interpolateRdBu(0.3);
            let color4 = d3.interpolateRdBu(0.4);
            let color5 = d3.interpolateRdBu(0.5);
            let color6 = d3.interpolateRdBu(0.6);
            let color7 = d3.interpolateRdBu(0.7);
            let color8 = d3.interpolateRdBu(0.8);
            let color9 = d3.interpolateRdBu(0.9);
            let color10 = d3.interpolateRdBu(1.0);

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

![](img/0485b1f2c287b0ae03c44b2c76126463.png)