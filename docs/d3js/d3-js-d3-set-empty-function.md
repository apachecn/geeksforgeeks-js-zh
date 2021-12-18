# D3.js | d3.set.empty()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-set-empty-function/](https://www.geeksforgeeks.org/d3-js-d3-set-empty-function/)

D3.js 中的 **set.empty()函数**用于在给定数组没有元素的情况下返回真，否则返回假。

**语法:**

```
d3.set([Array]).empty();
```

**参数:**该功能接受单参数**数组**，无论是否为空都将被搜索。

**返回值:**如果给定数组为空则返回真，否则返回假。

以下程序说明了 D3.js 中的 **d3.set.empty()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.set.empty() function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

         // Initialising an array
         Array1 = ["a"];
         Array2 = [];
         Array3 = ["Geeks", "gfg", "GeeksforGeeks"];

         // Calling the d3.set.empty() function
         A = d3.set(Array1).empty();
         B = d3.set(Array2).empty();
         C = d3.set(Array3).empty();

         // Getting the value true if the given array is 
         // empty otherwise returns false
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

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.set.empty() function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

        // Calling the d3.set.empty() function
        // with a array as the parameter 
        A = d3.set([1, 2, 3, 3]).empty();
        B = d3.set([]).empty();
        C = d3.set(["a", "b", "c", "a", "b", "c"]).empty();

        // Getting the value true if the given array is
        // empty otherwise returns false
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

**参考:**T2】https://devdocs.io/d3~5/d3-collection#set_empty