# D3.js | d3.map.get()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-get-function/](https://www.geeksforgeeks.org/d3-js-d3-map-get-function/)

D3.js 中的 **map.get()函数**用于返回指定键串的值。如果创建的映射不包含指定的键，则返回 undefined。

**语法:**

```
map.get(key)
```

**参数:**该功能接受单参数**键**，用于指定键串。

**返回值:**该函数返回指定键串的值。如果创建的映射没有指定键的条目，则返回 undefined。

下面的程序说明了 D3.js 中的 **d3.map.get()** 函数:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.get() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating a map
        var map = d3.map({"Ram": 5});

        // Calling the map.get() function
        A = map.get("Ram");

        // Getting the value for the "Ram" key
        console.log(A);
    </script>
</body>

</html>
```

**输出:**

```
5

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.get() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating a map
        var map1 = d3.map({"Ram": 5});
        var map2 = d3.map({"Geeks": 10});
        var map3 = d3.map({"Ram": 5}, {"Geeks": 10});
        var map4 = d3.map();

        // Calling the map.get() function
        A = map1.get("Ram");
        B = map2.get("Geeks");
        C = map3.get("Geeks");
        D = map3.get("Ram");
        E = map4.get("Geeks");

        // Getting the values for 
        // the specified keys
        console.log(A);
        console.log(B);
        console.log(C);
        console.log(D);
        console.log(E);
    </script>
</body>

</html>
```

**输出:**

```
5
10
undefined
5
undefined

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_get