# D3.js 插值 rBG()函数

> 原文:[https://www . geeksforgeeks . org/D3-js-插值 ebrbg-function/](https://www.geeksforgeeks.org/d3-js-interpolatebrbg-function/)

D3.js 中的 **d3 .插值 eBrBG()** 函数是一种发散配色方案，可用作连续插值器。该函数从 BrBG 发散配色方案中返回相应的颜色。

**语法:**

```
d3.interpolateBrBG(t);

```

**参数:**该函数接受一个参数，如上所述，如下所述。

*   **t:** 是一个在[0，1] 范围内的数字

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
        <title>D3.js interpolateBrBG() Function</title>
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
            console.log(d3.interpolateBrBG(0));
            console.log(d3.interpolateBrBG(0.1));
            console.log(d3.interpolateBrBG(0.001));
            console.log(d3.interpolateBrBG(0.2));
            console.log(d3.interpolateBrBG(0.211));
            console.log(d3.interpolateBrBG(0.3));
            console.log(d3.interpolateBrBG(1));
        </script>
    </body>
</html>
```

**输出:**

![](img/9ce41fce71756e5ff4a62ec43e458028.png)

**示例 2:**

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
        <title>D3.js interpolateBrBG() Function</title>
    </head>
    <style>
        div {
            padding: 10px;
            width: fit-content;
            height: 100px;
            float: left;
        }
    </style>
    <body>
        D3.interpolateBrBG()
        <br />
        <br />
        <div class="b1">
            <span>
                D3.interpolateBrBG(0.9)
            </span>
        </div>
        <div class="b2">
            <span>
                D3.interpolateBrBG(0.1)
            </span>
        </div>
        <div class="b3">
            <span>
                D3.interpolateBrBG(0.2)
            </span>
        </div>
        <div class="b4">
            <span>
                D3.interpolateBrBG(0.5)
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
            let color1 = d3.interpolateBrBG(0.9);

            let color2 = d3.interpolateBrBG(0.1);
            let color3 = d3.interpolateBrBG(0.2);
            let color4 = d3.interpolateBrBG(0.5);

            let b1 = document.querySelector(".b1");
            let b2 = document.querySelector(".b2");
            let b3 = document.querySelector(".b3");
            let b4 = document.querySelector(".b4");
            b1.style.backgroundColor = color1;
            b2.style.backgroundColor = color2;
            b3.style.backgroundColor = color3;
            b4.style.backgroundColor = color4;
        </script>
    </body>
</html>
```

**输出:**

![](img/1368b038144ca8838cdc6fcf3f011524.png)