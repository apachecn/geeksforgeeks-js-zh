# D3.js | d3.map.remove()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-remove-function/](https://www.geeksforgeeks.org/d3-js-d3-map-remove-function/)

**map.remove()函数**是 D3.js 中的一个内置函数。如果创建的映射包含给定的键字符串，那么它将删除条目并返回 true。如果键字符串不存在，则返回 false。

**语法:**

```
map.remove(key)
```

**参数:**该功能接受单参数**键**，用于指定键串。

**返回值:**如果创建的映射具有指定键字符串的条目，则该函数返回真，否则返回假。

以下程序说明了 D3.js 中的 **d3.map.remove()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.remove() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating a map
        var map = d3.map({"Ram": 5, "Geeks": 10, "gfg": 15});

        // Calling the map.remove() function
        A = map.remove("Ram");
        B = map.remove("Geek");
        C = map.remove("Geeks");

        // Getting true if the map has an
        // entry for the specified key string 
        // otherwise returns false.
        console.log(A);
        console.log(B);
        console.log(C);
    </script>
</body>

</html>
```

**输出:**

```
true
false
true

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.remove() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating some maps
        var map1 = d3.map({"Ram": 5});
        var map2 = d3.map({"Geeks": 10});
        var map3 = d3.map({"Ram": 5, "Geeks": 10});
        var map4 = d3.map();

        // Calling the map.remove() function
        A = map1.remove("Ram");
        B = map2.remove("Geek");
        C = map3.remove("Shyam");
        D = map4.remove("Ram");

        // Getting true if the map has an
        // entry for the specified key string 
        // otherwise returns false.
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
true
false
false
false

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_remove