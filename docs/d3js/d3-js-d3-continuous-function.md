# D3.js | d3.continuous()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-continuous-function/](https://www.geeksforgeeks.org/d3-js-d3-continuous-function/)

D3.js 中的 **d3.continuous()函数**用于在给定域值的情况下，从范围中返回相应的值。
**语法:**

```
d3.continuous().domain(array of values).range(array of values);
```

**参数:**此功能不接受任何参数。
**返回值:**该函数返回域值对应的范围值。
以下程序说明了 D3.js:
**示例 1:**
中的 **d3.continuous()** 功能

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.continuous() Function
    </title>

    <script src =
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Calling the scaleLinear() function
        var A = d3.scaleLinear().domain([10, 50])
                .range([0, 100]);

        // Getting the corresponding range for
        // the domain value
        console.log(A('15'));
        console.log(A('20'));
        console.log(A('25'));
        console.log(A('30'));
    </script>
</body>

</html>
```

**输出:**

```
12.5
25
37.5
50
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <title>
        D3.js | d3.continuous() Function
    </title>

    <script src =
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>

        // Calling the scaleLinear() function
        var A = d3.scaleLinear().domain([1, 5])
                .range([0, 10]);

        // Getting the corresponding range for
        // the domain value
        console.log(A('1'));
        console.log(A('2'));
        console.log(A('3'));
        console.log(A('4'));
    </script>
</body>

</html>
```

**输出:**

```
0
2.5
5
7.5
```

**参考:**T2https://devdocs.io/d3~5/d3-scale#_continuous