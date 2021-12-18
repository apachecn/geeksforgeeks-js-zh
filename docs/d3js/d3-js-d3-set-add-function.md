# D3.js | d3.set.add()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-set-add-function/](https://www.geeksforgeeks.org/d3-js-d3-set-add-function/)

D3.js 中的 **set.add()函数**用于将指定的值字符串添加到创建的集合中。

**语法:**

```
d3.set().add(element);
```

**参数:**该功能接受单参数**元素**，该元素将被添加到创建的集合中。

**返回值:**该函数不返回值。

下面的程序说明了 D3.js 中的 **d3.set.add()** 功能:

**例 1:**

```
<!DOCTYPE html>

<html>

<head>
    <title> d3.set.add() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Initialising the set
     var set = d3.set()
    .add("Geeks")
    .add("Geeks")
    .add("gfg");

    // Checking whether the desired element is 
    // present or not
    A = set.has("GeeksforGeeks");
    B = set.has("Ram");
    C = set.has("Geeks");

    // Getting the output of true or false
    console.log(A);
    console.log(B);
    console.log(C);
  </script>
</body>

</html>
```

**输出:**

```
false
false
true

```

**例 2:**

```
<!DOCTYPE html>

<html>

<head>
    <title> d3.set.add() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
  <script>

     // Initialising the set
     var set = d3.set().add("a").add(1).add(123);

    // Checking whether the desired element is 
    // present or not
    A = set.has("a");
    B = set.has(123);
    C = set.has(5);

    // Getting the output of true or false
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
true
false

```

**参考:**T2】https://devdocs.io/d3~5/d3-collection#set_add