# D3.js | d3.scaleIdentity()函数

> 原文:[https://www . geesforgeks . org/D3-js-D3-scale identity-function/](https://www.geeksforgeeks.org/d3-js-d3-scaleidentity-function/)

D3.js 中的 **d3.scaleIdentity()函数**用来构造单位域为[0，1]单位范围为[0，1]的新的身份尺度。
**语法:**

```
d3.scaleIdentity().domain(array of values).range(array of values);
```

**参数:**此功能不接受任何参数。
**返回值:**该函数返回该域值对应的范围。
下面的程序说明了 D3.js 中的 **d3.scaleIdentity()** 功能:
**示例:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
    <title></title>
    <script src="https://d3js.org/d3.v4.min.js">
  </script>
</head>

<body>

    <script>
        // Calling the scaleIdentity() function
        var A = d3.scaleIdentity()
            .domain([0, 1])
            .range([0, 1]);

        // Getting the corresponding range for
        // the domain value
        console.log(A('0'));
        console.log(A('1'));
    </script>
</body>

</html>
```

**输出:**

```
0
1
```

**参考:**T2https://devdocs.io/d3~5/d3-scale#scaleBand