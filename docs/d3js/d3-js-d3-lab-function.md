# D3.js | d3.lab()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-lab-function/](https://www.geeksforgeeks.org/d3-js-d3-lab-function/)

D3.js 中的 **d3.lab()函数**用于构造新的 lab 颜色，并返回指定颜色的‘l’、‘a’和‘b’属性作为函数的参数。

**语法:**

```
d3.lab(color);
```

**参数:**该功能接受单参数**颜色**，这是指定的 CSS 颜色。

**返回值:**该函数返回作为函数参数的指定 CSS 颜色的‘l’、‘a’和‘b’属性。

以下程序说明了 D3.js 中的 **d3.lab()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.lab() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.lab() function
        // with some parameters
        var color1 = d3.lab("red");
        var color2 = d3.lab("green");
        var color3 = d3.lab("blue");

        // Getting the LAB properties
        console.log(color1);
        console.log(color2);
        console.log(color3);
    </script>
</body>

</html>
```

**输出:**

```
{"l":53.24079414130722, "a":80.09245959641109, "b":67.20319651585301, "opacity":1}
{"l":46.22743146876261, "a":-51.69849552989111, "b":49.8968460010561, "opacity":1}
{"l":32.297010932850725, "a":79.18751984512224, "b":-107.8601617541481, "opacity":1}

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.lab() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.lab() function
        // without any parameters
        var color = d3.lab();

        // Getting the LAB values
        console.log(color);
    </script>
</body>

</html>
```

**输出:**

```
{"l":null, "a":null, "b":null, "opacity":1}

```

**参考:**T2】https://devdocs.io/d3~5/d3-color#lab