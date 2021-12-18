# D3.js | d3.set.clear()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-set-clear-function/](https://www.geeksforgeeks.org/d3-js-d3-set-clear-function/)

D3.js 中的 **set.clear()功能**用于从集合中移除所有值。在第二个例子中，它清除集合并保存空白集合。

**语法:**

```
d3.set().clear();
```

**参数:**此功能不接受任何参数。

**返回值:**该函数不返回值。

以下程序说明了 D3.js 中的 **d3.set.clear()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.set.clear() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Initialising the set
        var set = d3.set(["1", "2", "a", "b", "Geeks"]);

        // Checking the set
        console.log(set);
        // Calling the set.clear() function
        set.clear();

        // Checking whether any element is present
        // in the set or not
        A = set.has("a");
        B = set.has("Geeks");

        // Getting the output of true or false
        console.log(A);
        console.log(B);
    </script>
</body>

</html>
```

**输出:**

```
{"$1":"1","$2":"2","$a":"a","$b":"b","$Geeks":"Geeks"}
  false
  false

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title> d3.set.clear() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Initialising the set
     var set = d3.set(["1", "2", "a", "b", "Geeks"]);

     // Checking whether any element is present
     // in the set or not before calling set.clear() function
     A = set.has("a");
     B = set.has("Geeks");

     // Getting the output of true or false
     console.log(A);
     console.log(B);

     // Calling the set.clear() function
     set.clear();

     // Checking whether any element is present
     // in the set or not after calling set.clear() function
     C = set.has("a");
     D = set.has("Geeks");

     // Getting the output of true or false
     console.log(C);
     console.log(D);

  </script>
</body>

</html>
```

**输出:**

```
true
true
false
false

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#set_clear