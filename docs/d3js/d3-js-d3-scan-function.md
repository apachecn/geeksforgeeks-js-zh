# D3.js | d3.scan()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-scan-function/](https://www.geeksforgeeks.org/d3-js-d3-scan-function/)

**d3.scan()函数**是 D3.js 中的内置函数，线性扫描数组，根据指定的比较器返回最小元素的索引。当数组中没有可比较的元素时，函数返回 undefined。

**语法:**

```
d3.scan(array, comparator)
```

**参数:**该函数接受上面提到的和下面描述的两个参数:

*   **Array:** This mandatory parameter contains an array of elements whose minimum value will be calculated and the corresponding index will be returned.
*   **Comparator:** This parameter is an optional parameter that specifies how to obtain the minimum element.

**返回值:**该函数返回一个整数值，表示基于指定比较器的数组中最小元素的索引。

以下程序说明了 **d3.scan()** 功能的使用:

**示例 1:** 该程序说明了 d3.scan()与比较器

```
<!DOCTYPE html>
<html>

<head>
    <title>D3.js d3.scan() Function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>
        var array = [42, 71, 91, 67, 43, 17, 53];
        // To obtain the minimum element in the array
        var ans1 = d3.scan(array, function(a, b) {
            return a - b;
        });
        document.write("Minimum element is " + array[ans1] +
            " present at index: " + ans1 + "<br>");

        // To obtain the maximum element in the array
        var ans2 = d3.scan(array, function(a, b) {
            return b - a;
        });
        document.write("Maximum element is " + array[ans2] +
            " present at index: " + ans2);
    </script>
</body>

</html>
```

的使用

**输出:**

```
Minimum element is 17 present at index: 5
Maximum element is 91 present at index: 2

```

**示例 2:** 该程序说明了在没有比较器

```
<!DOCTYPE html> 
<html> 

<head> 
    <title>D3.js d3.scan() Function</title> 

    <script src='https://d3js.org/d3.v4.min.js'></script> 
</head> 

<body> 
<script> 

    var array = [42 , 71 , 91 , 67 , 43 , 17 , 53];
    // To obtain the minimum element in the array
    var ans1 = d3.scan(array, );
    document.write("Minimum element is " + array[ans1] + 
    " present at index: " + ans1);
</script> 
</body> 

</html>                    
```

的情况下 d3.scan()的使用

**输出:**

```
Minimum element is 17 present at index: 5

```

**参考:**T2】https://devdocs.io/d3~5/d3-array#scan