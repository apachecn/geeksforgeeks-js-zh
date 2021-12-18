# D3.js | d3.selectAll()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-selectall-function/](https://www.geeksforgeeks.org/d3-js-d3-selectall-function/)

D3.js 中的 **d3.selectAll()函数**用于选择与指定选择器字符串匹配的所有元素。

**语法:**

```
d3.selectAll("element")
```

**参数:**该功能接受单参数 *HTML 标签*作为参数。

**返回值:**该函数返回选中的元素。

以下程序说明了 D3.js 中的 **d3.selectAll()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.selectAll() Function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <div>Geeks</div>

    <div>GeeksforGeeks</div>

    <script>

        // Calling the selectAll() function
        d3.selectAll("div").text();
    </script>
</body>

</html>                    
```

**输出:**

```
Geeks
GeeksforGeeks

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.selectAll() Function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <p>GeeksforGeeks</p>

    <p>A computer science portal for geeks</p>

    <p>d3.selectAll() function</p>

    <script>

        // Calling the selectAll() function
        d3.selectAll("p").text();
    </script>
</body>

</html>                    
```

**输出:**

```
GeeksforGeeks
A computer science portal for geeks
d3.selectAll() function

```

**参考:**T2】https://devdocs.io/d3~5/d3-selection#selectAll