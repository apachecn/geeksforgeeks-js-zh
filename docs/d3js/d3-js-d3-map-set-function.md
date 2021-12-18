# D3.js | d3.map.set()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-map-set-function/](https://www.geeksforgeeks.org/d3-js-d3-map-set-function/)

D3.js 中的 **map.set()函数**用于在创建的映射中设置指定键串的值。

**语法:**

```
d3.map.set(key, value);
```

**参数:**该函数接受两个参数，如下图所示:

*   **键:**这是键串。
*   **值:**这是每个键串对应的值。

**返回值:**该函数不返回值。

下面的程序说明了 D3.js 中的 **d3.map.set()** 功能:
T3】示例 1:

```
<!DOCTYPE html>
<html>

<head>
   <title>d3.map.set() function</title>

   <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>

  <script>

     // Creating a map
     var map = d3.map()

     // setting the value for the specified key string
     // into above map
     .set("a", 1).set("b", 2).set("c", 3);

     // Getting the value for the specified key string
     A = map.get("a"); 
     B = map.get("c"); 

     // Printing the output of values
     console.log(A);
     console.log(B);
  </script>
</body>

</html>
```

**输出:**

```
1
3

```

**例 2:**

```
<!DOCTYPE html>

<html>

<head>
   <title>d3.map.set() function</title>

   <script src = "https://d3js.org/d3.v4.min.js"></script>
</head>

<body>

  <script>

     // Creating a map and setting the value
     // for the specified key string
     var map = d3.map().set("Geeks", 1).set("Geek", 2).set("gfg", 3);

     // Getting the value for the specified key string
     A = map.get("Geek"); 
     B = map.get("c"); 

     // Printing the output of values
     console.log(A);
     console.log(B);
  </script>
</body>

</html>
```

**输出:**

```
2
undefined

```

**注意:**在上面的代码中，字符串“c”不存在于创建的地图中，这就是为什么未定义被打印为输出的原因。

**参考:**T2】https://devdocs.io/d3~5/d3-collection#map_set