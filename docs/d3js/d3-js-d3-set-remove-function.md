# D3.js | d3.set.remove()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-set-remove-function/](https://www.geeksforgeeks.org/d3-js-d3-set-remove-function/)

**set.remove()** 是 D3.js 中的一个函数，如果给定的数组包含指定的值，则删除它并返回 true。否则，这个函数什么也不做，返回 false。

**语法:**

```
d3.set([Array]).remove(element);
```

**参数:**该函数接受两个参数，如下图所示:

*   **数组:**这是一个给定的字符串形式的元素数组。
*   **元素:**这是将被搜索到给定数组中的值，如果存在，则将其移除并返回真，否则不执行任何操作并返回假。

**返回值:**如果给定数组包含指定值，则返回真，否则返回假。
**注:**不装更新阵。
以下程序说明了 D3.js.
**中的 **d3.set.remove()** 功能示例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.set.remove() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>

  <script>

     // Initialising an array
     Array1 = ["a", "a", "b", "c"];
     Array2 = ["c", "c", "c"];
     Array3 = ["Geeks", "gfg", "GeeksforGeeks"];

     // Calling the d3.set.remove() function
     A = d3.set(Array1).remove("a");
     B = d3.set(Array2).remove("a");
     C = d3.set(Array3).remove("Geeks");

     // Getting the value true if the specified element
     // is present in the array otherwise false
     console.log(A);
     console.log(B);
     console.log(C);
  </script>
</body>
```

**输出:**

```
true
false
true

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.set.remove() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>
<body>

  <script>

     // Calling the d3.set.remove() function
     // with a array and a element as the parameter 
     A = d3.set([1, 2, 3, 3]).remove(4);
     B = d3.set(["a"]).remove("a");
     C = d3.set(["a", "b", "c", "a", "b", "c"]).remove("d");

     // Getting the value true if the specified element
     // is present in the array otherwise false
     console.log(A);
     console.log(B);
     console.log(C);
  </script>
</body>
```

**输出:**

```
false
true
false

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#set_remove