# D3.js | d3.map.entries()函数

> 原文:[https://www . geesforgeks . org/D3-js-D3-map-entries-function/](https://www.geeksforgeeks.org/d3-js-d3-map-entries-function/)

D3.js 中的 **map.entries()函数**用于为创建的映射中的条目返回键值对象数组。

**语法:**

```
d3.map.entries();
```

**参数:**此功能不接受任何参数。

**返回值:**该函数为创建的映射中的条目返回一个键值对数组。

下面的程序说明了 D3.js 中的 **d3.map.entries()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.entries() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Creating a map
     var map1 = d3.map({"a": 1});
     var map2 = d3.map({"GFG": 5});

     // Calling the map.entries() function
     A = map1.entries();
     B = map2.entries();

     // Getting the array of key value pair
     console.log(A);
     console.log(B);
  </script>
</body>

</html>
```

**输出:**

```
[{"key":"a", "value":1}]
[{"key":"GFG", "value":5}]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.entries() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Creating a map
     var map1 = d3.map({"Ram": 5}, {"Geek": 10});
     var map2 = d3.map();

     // Calling the map.entries() function
     A = map1.entries();
     B = map2.entries();

     // Getting the array of key value pair
     console.log(A);
     console.log(B);
  </script>
</body>

</html>
```

**输出:**

```
[{"key":"Ram", "value":5}]
[]

```

**注意:** Map2 为空，这就是它变成空白的原因。

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_entries