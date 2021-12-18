# D3.js | d3.set.values()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-set-values-function/](https://www.geeksforgeeks.org/d3-js-d3-set-values-function/)

D3.js 中的 **set.values()函数**用于返回集合中字符串值的数组。该函数可用于计算一组字符串的唯一值。

**语法:**

```
d3.set([Array]).values();
```

**参数:**该函数接受字符串的参数**数组**。

**返回值:**返回给定数组元素的唯一元素数组。

下面的程序说明了 D3.js:
**示例 1:** 中的 **d3.set.values()** 函数

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.set.values() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>

  <script>

     // Initialising an array
     Array1 = ["a", "a", "b", "c"];
     Array2 = ["c", "c", "c"];
     Array3 = ["Geeks", "gfg", "GeeksforGeeks"];

     // Calling the d3.set.values() function
     A = d3.set(Array1).values();
     B = d3.set(Array2).values();
     C = d3.set(Array3).values();

     // Getting the unique values of the set
     console.log(A);
     console.log(B);
     console.log(C);
  </script>
</body>
</html>
```

**输出:**

```
["a", "b", "c"]
["c"]
["Geeks", "gfg", "GeeksforGeeks"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.set.values() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>

  <script>

     // Calling the d3.set.values() function
     // with a array parameter
     A = d3.set([1, 2, 3, 3]).values();
     B = d3.set(["a"]).values();
     C = d3.set(["a", "b", "c", "a", "b", "c"]).values();

     // Getting the unique values of the set
     console.log(A);
     console.log(B);
     console.log(C);
  </script>
</body>
</html>
```

**输出:**

```
["1", "2", "3"]
["a"]
["a", "b", "c"]
```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#set_values