# D3.js | d3.set.size()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-set-size-function/](https://www.geeksforgeeks.org/d3-js-d3-set-size-function/)

D3.js 中的 **set.size()函数**用于统计唯一元素的个数，并返回给定数组中唯一元素的个数。

**语法:**

```
d3.set([Array]).size();
```

**参数:**该函数接受字符串的参数**数组**。

**返回值:**返回给定数组中唯一元素的个数。

以下程序说明了 D3.js 中的 **d3.set.size()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.set.size() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>

  <script>

     // Initialising an array
     Array1 = ["a", "a", "b", "c"];
     Array2 = ["c", "c", "c"];
     Array3 = ["Geeks", "gfg", "GeeksforGeeks"];

     // Calling the d3.set.size() function
     A = d3.set(Array1).size();
     B = d3.set(Array2).size();
     C = d3.set(Array3).size();

     // Getting the number of unique values in the array
     console.log(A);
     console.log(B);
     console.log(C);
  </script>
</body>
```

**输出:**

```
3
1
3

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.set.size() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>

  <script>

     // Calling the d3.set.size() function
     // with a array parameter
     A = d3.set([1, 2, 3, 3]).size();
     B = d3.set(["a"]).size();
     C = d3.set(["a", "b", "c", "a", "b", "c"]).size();

     // Getting the number of unique values in the array
     console.log(A);
     console.log(B);
     console.log(C);
  </script>
</body>
```

**输出:**

```
3
1
3

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#set_size