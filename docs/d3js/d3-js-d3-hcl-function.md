# D3.js | d3.hcl()功能

> 原文:[https://www.geeksforgeeks.org/d3-js-d3-hcl-function/](https://www.geeksforgeeks.org/d3-js-d3-hcl-function/)

D3.js 中的 **d3.hcl()函数**用于构造新的 hcl 颜色，并返回指定颜色的 HCL 属性作为函数的参数。

**语法:**

```
d3.hcl(color);
```

**参数:**该功能接受单参数**颜色**，用于指定 CSS 颜色。

**返回值:**该函数返回指定 CSS 颜色的 HCL 属性作为函数的参数。

以下程序说明了 D3.js 中的 **d3.hcl()** 功能:

**例 1:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.hcl() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.hcl() function
        // with some parameters
        var color1 = d3.hcl("red");
        var color2 = d3.hcl("green");
        var color3 = d3.hcl("blue");

        // Getting the HCL properties
        console.log(color1);
        console.log(color2);
        console.log(color3);
    </script>
</body>

</html>
```

**输出:**

```
{"h":39.99901061253295,"c":104.55176567686985,"l":53.24079414130722,"opacity":1}
{"h":136.01595303206318,"c":71.8500499715016,"l":46.22743146876261,"opacity":1}
{"h":306.2849380699878,"c":133.80761485376166,"l":32.297010932850725,"opacity":1}

```

**例 2:**

```
<!DOCTYPE html>
<html>

<head>
    <title>d3.hcl() function</title>

    <script src='https://d3js.org/d3.v4.min.js'></script>
</head>

<body>
    <script>

        // Calling the d3.hcl() function
        // without any parameters
        var color = d3.hcl();

        // Getting the HCL values
        console.log(color);
    </script>
</body>

</html>
```

**输出:**

```
{"h":null,"c":null,"l":null,"opacity":1}

```

**参考:**T2】https://devdocs.io/d3~5/d3-color#hcl