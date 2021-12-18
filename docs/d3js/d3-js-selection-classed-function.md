# D3.js 选择. D3.js()函数

> 原文:[https://www . geesforgeks . org/D3-js-selection-classed-function/](https://www.geeksforgeeks.org/d3-js-selection-classed-function/)

**selection.classed()** 功能用于设置所选元素的类别。此函数也可用于将类取消设置为选定的特定元素。

**语法:**

```
selection.classed(names[, value]);

```

**参数:**上面给定的函数采用上面给定并在下面描述的两个参数:

*   **名称:**是要赋予所选元素的类的名称。
*   **值:**设置或取消设置类的布尔值，即真或假。

**返回值:**这个函数不返回任何东西。

**例 1:** 设置类名。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" path1tent="width=device-width, 
                    initial-scale=1.0">
    <script src="https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <div>
        <a>GeeksforGeeks</a>
    </div>

    <script>

        // Sets the class to the a tag
        var a = d3.select("a")
            .classed("className", true);

        // This will select the anchor tag
        var divselect = document.querySelector(".className");
        console.log(divselect.innerHTML);
    </script>
</body>

</html>
```

**输出:**

```
GeeksforGeeks
```

**示例 2:** 取消设置类名。

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport" path1tent="width=device-width, 
                    initial-scale=1.0">
    <script src="https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <div>
        <p class="classGiven classGiven2">
            GeeksforGeeks
        </p>
    </div>

    <script>

        // Unsets the class named classGiven
        // to the "p" tag
        var a = d3.select("p")
            .classed("classGiven2", false);

        // This will select the "p" tag
        var divselect = document
            .querySelector(".classGiven");

        console.log(divselect.innerHTML);

        // This will not select the "p" tag
        // As the classGiven 2 is unset

        var divselect = document
            .querySelector(".classGiven2");

        console.log(divselect);
    </script>
</body>

</html>
```

**输出:**

```
GeeksforGeeks
null
```