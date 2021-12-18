# D3.js | d3.map.has()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-has-function/](https://www.geeksforgeeks.org/d3-js-d3-map-has-function/)

D3.js 中的 **map.has()函数**用于在创建的映射有指定键串的条目时返回 true。map.has()函数的值可能为 null 或未定义。

**语法:**

```
map.has(key)
```

**参数:**该功能接受单参数**键**，指定键串。

**返回值:**如果创建的映射有指定键串的条目，该函数返回真。该值可能为空或未定义。

以下程序说明了 D3.js 中的 **d3.map.has()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.has() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating a map
        var map = d3.map({"Ram": 5});

        // Calling the map.has() function
        A = map.has("Ram");
        B = map.has("Geeks");

        // Getting the true if the map
        // has an entry for the specified key string
        // else false
        console.log(A);
        console.log(B);
    </script>
</body>

</html>
```

**输出:**

```
true
false

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.has() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating a map
        var map1 = d3.map({"Ram": 5});
        var map2 = d3.map({"Geeks": 10});
        var map3 = d3.map({"Ram": 5}, {"Geeks": 10});
        var map4 = d3.map();

        // Calling the map.has() function
        A = map1.has("Ram");
        B = map2.has("Geeks");
        C = map3.has("Geeks");
        D = map3.has("Ram");
        E = map4.has("Geeks");

        // Getting the true if the map
        // has an entry for the specified key string
        // else false
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
true
true
false
true
false

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_has