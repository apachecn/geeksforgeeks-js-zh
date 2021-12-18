# D3.js | d3.keys()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-keys-function/](https://www.geeksforgeeks.org/d3-js-d3-keys-function/)

D3.js 中的 **d3.keys()函数**用于返回一个包含指定对象的属性名或键的数组或一个关联数组。

**语法:**

```
d3.keys(object)
```

**参数:**该功能成对接受包含键和值的单参数**对象**。

**返回值:**返回给定对象的按键。

下面的程序说明了 D3.js 中的 d3.keys()函数:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.keys() Function
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

        // Calling the d3.keys() function
        A = d3.keys(month);

        // Getting the key values of the given object
        document.write(A);
    </script>
</body>

</html>                    
```

**输出:**

```
January, February, March, April

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.keys() Function
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

        // Calling the d3.keys() function
        A = d3.keys(month);

        // Getting the key values of the given object
        document.write(A);
    </script>
</body>

</html>                    
```

**输出:**

```
GeeksforGeeks, Geeks, Geek, gfg

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#keys