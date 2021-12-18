# D3.js | d3.map.clear()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-clear-function/](https://www.geeksforgeeks.org/d3-js-d3-map-clear-function/)

D3.js 中的 **map.clear()函数**用于从创建的地图中移除所有条目。

**语法:**

```
d3.map.clear();
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

以下程序说明了 D3.js 中的 **d3.map.clear()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.map.clear() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Creating a map
     var map = d3.map({"a": 1}, {"b": 2}, {"c": 3});

     // Calling the map.clear() function
     map.clear();

     // Checking whether the value for the specified key 
     // is present or not
     A = map.get("a");

    // Getting the output either value of the specified key
    // string or undefined if the key is not present
    console.log(A);

  </script>
</body>

</html>
```

**输出:**

```
undefined

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.map.clear() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Constructing a map
     var map = d3.map({"a": 0}, {"b": 1}, {"c": 2});

     // Checking whether the value for the specified key
     // is present or not before calling clear() function
     A = map.get("a");

     // Getting the output of value
     console.log(A);

     // Calling the map.clear() function
     map.clear();

     // Checking whether the value for the specified key
     // is present or not after calling clear() function
     B = map.get("a");

     // Getting the output of value
     console.log(B);
  </script>
</body>

</html>
```

**输出:**

```
0
undefined

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_clear