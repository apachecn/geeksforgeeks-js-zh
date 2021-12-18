# D3.js | d3.entries()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-entries-function/](https://www.geeksforgeeks.org/d3-js-d3-entries-function/)

**免责声明**:在 D3.js 函数 D3 的**第 6 版**中，词条被弃用。应该改用 Object.entries。

D3.js 中的 **d3.entries 函数**用于返回一个包含指定对象的属性名和属性值的数组。
**语法:**

```
d3.entries(object)
```

**参数:**该函数接受一个参数——一个 JavaScript **对象**。
**返回值:**返回包含指定对象的属性名和值的数组。
下面的程序说明了 D3.js 中的 d3.entries 函数:
**例 1:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.entries() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>

<script>

     // Initialising an object
     var month = {"January": 1, "February": 2, "March": 3};

     // Calling the d3.entries() function
     A = d3.entries(month);

     // Getting the key and value in pairs
     console.log(A);
  </script>
</body>
</html>
```

**输出:**

```
[{"key":"January","value":1},{"key":"February","value":2},
                                       {"key":"March","value":3}]
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.entries function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>
  <script>

     // Initialising an object
     var month = {"GeeksforGeeks": 0, "Geeks": 2,
                                     "Geek": 3, "gfg": 4};

     // Calling the d3.entries function
     A = d3.entries(month);

     // Getting the key and value in pairs.
     console.log(A);
  </script>
</body>
</html>
```

**输出:**

```
[{"key":"GeeksforGeeks","value":0},{"key":"Geeks","value":2},
                     {"key":"Geek","value":3},{"key":"gfg","value":4}]
```

**参考:**T2https://devdocs.io/d3~5/d3-collection#entries