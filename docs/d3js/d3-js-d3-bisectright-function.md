# D3.js | d3 .平分右()功能

> 原文:[https://www . geesforgeks . org/D3-js-D3-divider right-function/](https://www.geeksforgeeks.org/d3-js-d3-bisectright-function/)

**平分右()函数**是 D3.js 中的内置函数，它接受一个值作为其参数之一，并返回索引以将元素插入作为另一个参数传递的数组中，从而在指定范围或整个数组中保持排序顺序。

默认情况下，函数在查找索引时会考虑整个数组，除非通过将开始和结束作为参数传递给函数来指定范围。

函数二进制搜索值，并检查该值是否已经存在于该范围内。如果找到，它将被插入到该元素的右侧。

**语法:**

```
d3.bisectRight(array, value, start, end)
```

**参数:**这个函数接受上面提到的和下面描述的四个参数:

*   **Array:** This *mandatory parameter* contains an array of elements.
*   **Value:** This is also a *mandatory parameter* , which contains the value to be inserted into the array.
*   **Start:** This is a *optional parameter* , which specifies the starting index of the range.
*   **end:** This is a *optional parameter* , the last indicator of the specified range.

**返回值:**该函数返回一个整数值，表示需要在数组中插入**值**以保持排序顺序的索引。

以下程序说明了 **d3 .平分右()**功能的使用:

**示例 1:** 这个程序说明了 d3 .平分右()只传递两个强制参数的用法。

```
<!DOCTYPE html>
<html>

<head>
    <title>D3.js d3.bisectRight() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>
        var array = [42, 43, 53, 61, 71, 87, 91];
        var value1 = 63;
        var pos = d3.bisectRight(array, value1);
        document.write(value1 + " needs to be inserted at " 
        + pos + "<br>");

        var value2 = 80;
        var pos2 = d3.bisectRight(array, value2);
        document.write(value2 + " needs to be inserted at " 
        + pos2);
    </script>
</body>

</html>
```

**输出:**

```
63 needs to be inserted at 4
80 needs to be inserted at 5

```

**示例 2:** 这个程序演示了 d3 .平分右()将所有四个参数传递给函数的用法。

```
<!DOCTYPE html>
<html>

<head>
    <title>D3.js d3.bisectRight() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>
        var array = [42, 34, 27, 53, 61, 71, 33, 51, 87, 91];
        var value1 = 63;
        var pos = d3.bisectRight(array, value1, 2, 5);
        document.write(value1 + " needs to be inserted at " 
        + pos + "<br>");

        var pos2 = d3.bisectRight(array, value1, 6, 9);
        document.write(value1 + " needs to be inserted at " 
        + pos2);
    </script>
</body>

</html>
```

**输出:**

```
63 needs to be inserted at 5
63 needs to be inserted at 8

```

**示例 3:** 本程序说明了 **d3 .平分右()**和 **d3 .平分左()**功能之间的区别。

```
<!DOCTYPE html>
<html>

<head>
    <title>
    Difference between d3.bisectRight() 
    and d3.bisectLeft() functions
    </title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>
        var array = [42, 54, 59, 63, 71, 81, 91];
        var value = 63;
        var pos = d3.bisectLeft(array, value);
        document.write(value + " needs to be inserted at " 
        + pos + "<br>");

        var pos2 = d3.bisectRight(array, value);
        document.write(value + " needs to be inserted at " 
        + pos2);
    </script>
</body>

</html>                    
```

**输出:**

```
63 needs to be inserted at 3
63 needs to be inserted at 4

```

**参考:**T2】https://devdocs.io/d3~5/d3-array#bisectRight