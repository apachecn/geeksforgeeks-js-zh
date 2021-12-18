# D3.js | d3.map.keys()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-keys-function/](https://www.geeksforgeeks.org/d3-js-d3-map-keys-function/)

D3.js 中的 **map.keys()函数**用于为创建的映射中的每个条目返回一个字符串键数组。返回密钥的顺序是任意的。

**语法:**

```
map.keys()
```

**参数:**此功能不接受任何参数。

**返回值:**该函数为创建的映射中的每个条目返回一个字符串键数组。

以下程序说明了 D3.js 中的 **d3.map.keys()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.keys() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating a map
        var map = d3.map({"Ram": 5, "Geeks": 10, "gfg": 15});

        // Calling the map.keys() function
        A = map.keys();

        // Getting an array of string keys for
        // every entry in the map.
        console.log(A);
    </script>
</body>

</html>
```

**输出:**

```
["Ram", "Geeks", "gfg"]

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.map.keys() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Creating some maps
        var map1 = d3.map({"Ram": 5});
        var map2 = d3.map({"Geeks": 10});
        var map3 = d3.map({"Ram": 5, "Geeks": 10});
        var map4 = d3.map();

        // Calling the map.keys() function
        A = map1.keys();
        B = map2.keys();
        C = map3.keys();
        D = map4.keys();

        // Getting an array of string keys for
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
["Ram"]
["Geeks"]
["Ram", "Geeks"]
[]

```

**参考:t1】[https://devdocs . io/D3 ~ 5/D3 集合#map_keys](https://devdocs.io/d3~5/d3-collection#map_keys)**