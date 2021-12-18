# D3.js 选择.回车()功能

> 原文:[https://www . geesforgeks . org/D3-js-selection-enter-function/](https://www.geeksforgeeks.org/d3-js-selection-enter-function/)

D3.js 中的 **d3.selection.enter()** 函数用于创建缺失的元素并返回回车选择。

**语法:**

```
selection.enter(); 

```

**参数:**此功能不接受任何参数。

**返回值:**该功能返回回车选择。

下面的例子说明了 JavaScript 中的 D3.js selection.enter()函数:

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
        <title>D3.js selection.enter() Function</title>
    </head>
    <style>
        div {
            background-color: green;
            color: #ffffff;
            width: 50px;
            margin-bottom: 5px;
            padding: 20px;
            height: 10px;
        }
    </style>
    <body>
        <!-- Please note that no div tags are added here -->
        <script src=
"https://d3js.org/d3.v4.min.js">
        </script>
        <script src=
"https://d3js.org/d3-selection.v1.min.js">
        </script>
        <script>
            var div = d3
                .select("body")
                .selectAll("div")
                .data(["geeks", "for", "geeks"])
                .enter()
                .append("div")
                .text((d) => {
                    return d;
                });
        </script>
    </body>
</html>
```

**输出:**

![](img/b2e198b100e2c45380db40b3e81af855.png)

**例 2:**

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
        <title>D3.js selection.enter() Function</title>
    </head>
    <style>
        div {
            background-color: green;
            color: #ffffff;
            width: 50px;
            margin-bottom: 5px;
            padding: 20px;
            height: 10px;
        }
    </style>
    <body>
        <!-- Please note that no div tags are added here -->
        <script src=
"https://d3js.org/d3.v4.min.js">
        </script>
        <script src=
"https://d3js.org/d3-selection.v1.min.js">
        </script>
        <script>
            var h2 = d3
                .select("body")
                .selectAll("h2")
                .data(["I am from heading level 2"])
                .enter()
                .append("h2")
                .text((d) => {
                    return d;
                });
            var span = d3
                .select("body")
                .selectAll("span")
                .data("I am from span")
                .enter()
                .append("span")
                .text((d) => {
                    return d;
                });
            var p = d3
                .select("body")
                .selectAll("p")
                .data(["paragraph", "paragraph"])
                .enter()
                .append("p")
                .text((d) => {
                    return d;
                });
        </script>
    </body>
</html>
```

**输出:**

![](img/01c884f6d65928fa6433798a4a9d99d8.png)