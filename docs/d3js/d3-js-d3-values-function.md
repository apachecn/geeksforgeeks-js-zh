# D3.js | d3.values()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-values-function/](https://www.geeksforgeeks.org/d3-js-d3-values-function/)

D3.js 中的 **d3.values()函数**用于返回包含指定对象属性值的数组或关联数组。

**语法:**

```
d3.values(object)
```

**参数:**该函数接受单参数**对象**，该对象包含键、值对。

**返回值:**返回给定对象的值。

下面的程序说明了 D3.js 中的 d3.values()函数:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.values() function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

        // Initialising an object
        var month = {
            "January": 1,
            "February": 2,
            "March": 3,
            "April": 4
        };

        // Calling the d3.values() function
        A = d3.values(month);

        // Getting the values of the given object
        document.write(A);
    </script>
</body>

</html>                    
```

**输出:**

```
1, 2, 3, 4

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.values() function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

        // Initialising an object
        var month = {
            "GeeksforGeeks": 0,
            "Geeks": 2,
            "Geek": 3,
            "gfg": 4
        };

        // Calling the d3.values() function
        A = d3.values(month);

        // Getting the values of the given object
        document.write(A);
    </script>
</body>

</html>                     
```

**输出:**

```
0, 2, 3, 4

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#values