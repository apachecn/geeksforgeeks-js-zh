# D3.js | d3.map.empty()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-empty-function/](https://www.geeksforgeeks.org/d3-js-d3-map-empty-function/)

D3.js 中的 **map.empty()函数**用于在创建的地图包含零条目时返回真，否则返回假。

**语法:**

```html
map.empty();
```

**参数:**此功能不接受任何参数。

**返回值:**如果地图为空，该函数返回真，否则返回假。

以下程序说明了 D3.js 中的 **d3.map.empty()** 功能:

**例 1:**

```html
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.map.empty() Function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

        // Creating a map
        var map1 = d3.map({"a": 1}, {"b": 2}, {"c": 3});
        var map2 = d3.map();

        // Calling the map.empty() function
        A = map1.empty();
        B = map2.empty();

        // Getting the result whether the maps are empty or not
        console.log(A);
        console.log(B);
    </script>
</body>    

</html>
```

**输出:**

```html
false
true

```

**例 2:**

```html
<!DOCTYPE html>
<html>

<head>
    <title>
        d3.map.empty() Function
    </title>

    <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>
    <script>

        // Creating a map
        var map1 = d3.map({"a": 1}, {"b": 2}, {"c": 3});
        var map2 = d3.map({"GFG": 5});
        var map3 = d3.map({});
        var map4 = d3.map();

        // Calling the map.empty() function
        A = map1.empty();
        B = map2.empty();
        C = map3.empty();
        D = map4.empty();

        // Getting the result whether
        // the maps are empty or not
        console.log(A);
        console.log(B);
        console.log(C);
        console.log(D);
    </script>
</body>    

</html>
```

**输出:**

```html
false
false
true
true

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_empty