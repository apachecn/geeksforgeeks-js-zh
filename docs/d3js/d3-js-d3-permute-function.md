# D3.js | d3.permute()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-permute-function/](https://www.geeksforgeeks.org/d3-js-d3-permute-function/)

D3.js 中的 **d3.permute()函数**用于用给定的指定索引数组置换给定数组的元素，并返回包含每个给定索引对应元素的数组。

**语法:**

```
d3.permute(array, Index)
```

**参数:**这个函数接受上面提到的和下面描述的两个参数:

*   **Array:** is an array of elements to be arranged.
*   **Index:** is a given index, which is used to replace the given array elements and return the elements of the given array to the array accordingly.

**返回值:**返回置换元素的数组。

下面的程序说明了 D3.js 中的 **d3.permute()** 函数。

**示例 1:** 在下面的代码中，使用给定的指定索引数组对给定数组的元素进行置换，并返回包含每个给定索引的对应元素的数组。

```
<html>

<head>
    <title>
      Getting permuted array of elements
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // Initialising the arrays of elements
        var Array1 = ["gfg", "Geek", "Geeks", "GeeksforGeeks"];
        var Array2 = ["a", "ab", "abc", "abcd"];

        // Initialising the indexes
        var Index1 = [1, 2, 0, 3];
        var Index2 = [3, 1, 2, 0];

        // Calling to d3.permute() function
        A = d3.permute(Array1, Index1);
        B = d3.permute(Array2, Index2);

        // Getting permuted array of elements
        document.write(A + "<br>");
        document.write(B + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
Geek, Geeks, gfg, GeeksforGeeks
abcd, ab, abc, a
```

**例 2:**

```
<html>

<head>
    <title>
      Getting permuted array of elements
  </title>
</head>

<body>
    <script src='https://d3js.org/d3.v4.min.js'>
  </script>

    <script>
        // Taking the array of elements and 
        // indexes as the parameters
        // for the function d3.permute()
        A = d3.permute(["Hi", "Hello", "Greet"], [1, 2, 0]);
        B = d3.permute(["Ram", "Shyam", "Geeta", "Hari"],
                       [3, 1, 2, 0]);

        // Getting permuted array of elements
        document.write(A + "<br>");
        document.write(B + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
Hello, Greet, Hi
Hari, Shyam, Geeta, Ram
```

**参考:t1】[https://devdocs . io/D3 ~ 4/D3 阵列# switch](https://devdocs.io/d3~4/d3-array#permute)**