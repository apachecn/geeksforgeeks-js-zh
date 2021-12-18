# D3.js | d3.map.size()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-size-function/](https://www.geeksforgeeks.org/d3-js-d3-map-size-function/)

D3.js 中的 **map.size()函数**用于返回创建的地图中的条目数。

**语法:**

```
map.size()
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回创建的地图中的条目数。

下面的程序说明了 D3.js 中的 **d3.map.size()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.size() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating a map
        var map = d3.map({"Ram": 5, "Geeks": 10, "gfg": 15});

        // Calling the map.size() function
        A = map.size();

        // Getting the the number of
        // entries in the map.
        console.log(A);
    </script>
</body>

</html>
```

**输出:**

```
3

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.size() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating some maps
        var map1 = d3.map({"Ram": 5});
        var map2 = d3.map({"Geeks": 10});
        var map3 = d3.map({"Ram": 5, "Geeks": 10});
        var map4 = d3.map();

        // Calling the map.size() function
        A = map1.size();
        B = map2.size();
        C = map3.size();
        D = map4.size();

        // Getting the number of entries in the map.
        console.log(A);
        console.log(B);
        console.log(C);
        console.log(D);
    </script>
</body>

</html>
```

**输出:**

```
1
1
2
0

```

**参考:t1】[https://devdocs . io/D3 ~ 5/D3 集合#map_size](https://devdocs.io/d3~5/d3-collection#map_size)**