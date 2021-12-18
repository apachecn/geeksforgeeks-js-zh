# D3.js 插值 Gy()函数

> 原文:[https://www . geesforgeks . org/D3-js-interpredergy-function/](https://www.geeksforgeeks.org/d3-js-interpolaterdgy-function/)

d3.js 中的 D3 .插值颜色()函数是发散配色方案的一部分，它从 D3.js 中的 RdBu 发散配色方案返回颜色，这里 Rd 可以解释为红色，Gy 可以解释为灰色。

**语法:**

```
d3.interpolateRdGy(t);

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **t:** 这是一个介于 0 和 1 之间的数字。

**返回值:**上述函数返回 RGB 字符串。

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
        <title>D3.js interpolateRdGy() Function</title>
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

            console.log(d3.interpolateRdGy(0));
            // When t is 0.0
            console.log(d3.interpolateRdGy(0.1));
            // When t is 0.1
            console.log(d3.interpolateRdGy(0.2));
            // When t is 0.2
            console.log(d3.interpolateRdGy(0.3));
            // When t is 0.3
            console.log(d3.interpolateRdGy(0.4));
            // When t is 0.4
            console.log(d3.interpolateRdGy(0.5));
            // When t is 0.5
            console.log(d3.interpolateRdGy(0.6));
            // When t is 0.6
            console.log(d3.interpolateRdGy(0.7));
            // When t is 0.7
            console.log(d3.interpolateRdGy(0.8));
            // When t is 0.8
            console.log(d3.interpolateRdGy(0.9));
            // When t is 0.9
            console.log(d3.interpolateRdGy(1.0));
            // When t is 1.0
        </script>
    </body>
</html>
```

**输出:**不同 t 值的颜色的 RGB。

![](img/73a928083b2be0d372c287ed6bff664d.png)

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
        <title>D3.js interpolateRdGy() Function</title>
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
        <h2>D3.interpolateRdGy()</h2>
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
            // creating different colors for different
            // Values of t as 0.1,0.2... 1.0
            let color1 = d3.interpolateRdGy(0.1);
            let color2 = d3.interpolateRdGy(0.2);
            let color3 = d3.interpolateRdGy(0.3);
            let color4 = d3.interpolateRdGy(0.4);
            let color5 = d3.interpolateRdGy(0.5);
            let color6 = d3.interpolateRdGy(0.6);
            let color7 = d3.interpolateRdGy(0.7);
            let color8 = d3.interpolateRdGy(0.8);
            let color9 = d3.interpolateRdGy(0.9);
            let color10 = d3.interpolateRdGy(1.0);

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

![](img/5cea498c2c8c69b5dc0e19c95dc3f50e.png)