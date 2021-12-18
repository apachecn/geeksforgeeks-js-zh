# D3.js | d3.continuous.clamp()函数

> 原文:[https://www . geesforgeks . org/D3-js-D3-continuous-clamp-function/](https://www.geeksforgeeks.org/d3-js-d3-continuous-clamp-function/)

D3.js 中的 **d3.continuous.clamp()功能**用于启用或禁用夹钳。如果箝位被禁用，则域值的范围可能超出范围，但如果箝位被启用，则域值的范围将始终在范围内。

**语法:**

```
continuous.clamp( Value )
```

**参数:**该功能接受单个参数**值**，该值为真或假。

**返回值:**该函数不返回值。

以下程序说明了 D3.js 中的 **d3.continuous.clamp()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.continuous.clamp() Function
    </title>

    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Calling the .scaleLinear() function
        var x = d3.scaleLinear()
            .domain([10, 100])
            .range([0, 5]);

        // Calling the .clamp() function          
        x.clamp(false);

        // Calling continuous() and .invert() function
        var A = x(6);
        var B = x.invert(10);
        console.log(A);
        console.log(B);
    </script>
</body>

</html>
```

**输出:**

```
-0.22222222222222224
190

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.continuous.clamp() Function
    </title>

    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Calling the .scaleLinear() function
        var x = d3.scaleLinear()
            .domain([10, 100])
            .range([0, 5]);

        // Calling the .clamp() function          
        x.clamp(true);

        // Calling continuous() and .invert() function
        var A = x(6);
        var B = x.invert(10);
        console.log(A);
        console.log(B);
    </script>
</body>

</html>
```

**输出:**

```
0
100

```

**参考:**T2】https://devdocs.io/d3~5/d3-scale#continuous_clamp