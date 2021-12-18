# D3.js | d3.select()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-select-function/](https://www.geeksforgeeks.org/d3-js-d3-select-function/)

D3.js 中的 **d3.select()函数**用于选择与指定选择器字符串匹配的第一个元素。如果有任何元素不匹配，则返回空选择。如果选择器匹配了多个元素，那么将只选择第一个匹配的元素。

**语法:**

```
d3.select("element")
```

**参数:**该函数接受保存元素名称的单个参数。

**返回值:**该函数返回选中的元素。

以下程序说明了 D3.js 中的 **d3.select()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.select() Function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>

    <div>GeeksforGeeks</div>

    <script>

        // Calling the select() function
        var a = d3.select("div").text();

        // Getting the selected element
        console.log(a);
    </script>
</body>

</html>                    
```

**输出:**

```
GeeksforGeeks 

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>

    <title>
        D3.js | d3.select() Function
    </title>

    <script src="https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <p>GeeksforGeeks</p>

    <p>A computer science portal for geeks</p>

    <script>

        // Calling the select() function
        var a = d3.select("p").text();

        // Getting the selected element
        console.log(a);
    </script>
</body>

</html>
```

**输出:**

```
GeeksforGeeks
```

**参考:**T2】https://devdocs.io/d3~5/d3-selection#select