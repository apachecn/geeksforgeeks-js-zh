# D3.js 选择. size()功能

> 原文:[https://www . geesforgeks . org/D3-js-selection-size-function/](https://www.geeksforgeeks.org/d3-js-selection-size-function/)

D3.js 中的 **selection.size()** 函数用于计算并返回选择的大小。它计算所选内容中的总元素并返回其大小。

**语法:**

```
selection.size();
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回一个数值。

**例 1:** 当选择非空时。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" path1tent=
        "width=device-width,initial-scale=1.0">
    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
    <script src=
"https://d3js.org/d3-selection.v1.min.js">
    </script>
</head>

<body>
    <div>Geeks for Geeks </div>
    <div></div>
    <div></div>
    <div></div>
    <div></div>

    <script>
        let selection = d3.selectAll("div")
        let div = selection.size();
        console.log(div)
    </script>
</body>

</html>
```

**Output:**

```
5
```

**例 2:** 选择为空时。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" path1tent=
        "width=device-width,initial-scale=1.0">
    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
    <script src=
"https://d3js.org/d3-selection.v1.min.js">
    </script>
</head>

<body>
    <script>
        let selection=d3.selectAll("h2")
        let size=selection.size();
        console.log(size)
      </script> 
</body>

</html>
```

**输出:**

```
0
```