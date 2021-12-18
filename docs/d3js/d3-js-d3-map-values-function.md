# D3.js | d3.map.values()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-values-function/](https://www.geeksforgeeks.org/d3-js-d3-map-values-function/)

D3.js 中的 **map.values()函数**用于为创建的映射中的每个条目返回一个值数组。返回值的顺序是任意的。

**语法:**

```
d3.map.values()
```

**参数:**此功能不接受任何参数。

**返回值:**该函数为创建的地图中的每个条目返回一个值数组。这些返回值的顺序是任意的。

下面的程序说明了 D3.js 中的 **d3.map.values()** 函数:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.map.values() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>   
  <script>

     // Creating a map
     var map = d3.map({"Ram": 5, "Geeks": 10, "gfg": 15});

     // Calling the map.values() function
     A = map.values();

     // Getting an array of values for
     // every entry in the map.
     console.log(A);
  </script>
</body>

</html>
```

**输出:**

```
[5, 10, 15]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.map.values() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Creating some maps
     var map1 = d3.map({"Ram": 5});
     var map2 = d3.map({"Geeks": 10});
     var map3 = d3.map({"Ram": 5, "Geeks": 10});
     var map4 = d3.map();

     // Calling the map.values() function
     A = map1.values();
     B = map2.values();
     C = map3.values();
     D = map4.values();

     // Getting an array of values for
     // every entry in the map.
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
[5]
[10]
[5, 10]
[]

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_values