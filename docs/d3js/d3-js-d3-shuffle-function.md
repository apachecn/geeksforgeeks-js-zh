# D3.js | d3.shuffle()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-shuffle-function/](https://www.geeksforgeeks.org/d3-js-d3-shuffle-function/)

D3.js 中的 **d3.shuffle()函数**用于对给定数组元素的顺序进行随机化或洗牌，并返回数组。

**语法:**

```
d3.shuffle( Array, start, stop )
```

**参数:**该函数接受三个参数，如上所述，如下所述:

*   **Array:** This parameter holds array elements.
*   **start:** represents the starting index of the array and shuffles the array elements. If no starting value is specified, zero is taken as the default value.
*   **stop:** indicates the end index of array for shuffling array elements. Its default value is the length of the array.

**返回值:**返回混洗元素的数组。

下面的程序说明了 D3.js 中的 d3.shuffle()函数:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.shuffle() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Initialising some array of elements
        Array1 = [1, 2, 3, 4];
        Array2 = [10, 20, 30, 40];
        Array3 = [5, 7, 9, 11];
        Array4 = [2, 4, 6, 8, 10];

        // Calling to d3.shuffle() function
        A = d3.shuffle(Array1);
        B = d3.shuffle(Array2, 1, 3);
        C = d3.shuffle(Array3);
        D = d3.shuffle(Array4, 2, 5);

        // Getting the shuffled elements
        document.write(A + "<br>");
        document.write(B + "<br>");
        document.write(C + "<br>");
        document.write(D + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
2, 3, 1, 4
20, 40, 10, 30
11, 9, 5, 7
2, 10, 4, 8, 6

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.shuffle() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Initialising some array of elements
        Array1 = ["a", "b", "c"];
        Array2 = ["z", "y", "x"];

        // Calling to d3.shuffle() function
        A = d3.shuffle(Array1);
        B = d3.shuffle(Array2);

        // Getting the shuffled elements
        document.write(A + "<br>");
        document.write(B + "<br>");
    </script>
</body>

</html>
```

**输出:**

```
b, a, c
z, y, x
```

**参考:**T2】https://devdocs.io/d3~5/d3-array#shuffle