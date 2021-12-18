# D3.js | d3.set.has()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-set-has-function/](https://www.geeksforgeeks.org/d3-js-d3-set-has-function/)

D3.js 中的 **set.has()函数**用于当且仅当给定的集合包含指定值的条目时返回 true。

**语法:**

```
d3.set([Array]).has(element);
```

**参数:**这个函数接受上面提到的和下面描述的两个参数:

*   **Array:** It stores array elements in the form of strings.
*   **Element:** This is the value to be searched in the given array. If it exists, it returns true; otherwise, it returns false.

**返回值:**如果给定数组包含指定值，则返回真，否则返回假。

以下程序说明了 D3.js 中的 **d3.set.has()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.set.has() function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

        // Initialising an array
        Array1 = ["a", "a", "b", "c"];
        Array2 = ["c", "c", "c"];
        Array3 = ["Geeks", "gfg", "GeeksforGeeks"];

        // Calling the d3.set.has() function
        A = d3.set(Array1).has("a");
        B = d3.set(Array2).has("a");
        C = d3.set(Array3).has("Geeks");

        // Getting the value true if the specified element
        // is present in the array otherwise false
        console.log(A);
        console.log(B);
        console.log(C);
    </script>
</body>

</html>
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
    <title>
        d3.set.has() function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

        // Calling the d3.set.has() function
        // with a array and a element as the parameter 
        A = d3.set([1, 2, 3, 3]).has(4);
        B = d3.set(["a"]).has("a");
        C = d3.set(["a", "b", "c", "a", "b", "c"]).has("d");

        // Getting the value true if the specified element
        // is present in the array otherwise false
        console.log(A);
        console.log(B);
        console.log(C);
    </script>
</body>

</html>
```

**输出:**

```
false
true
false

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#set_has