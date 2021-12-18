# D3.js 带宽()函数

> 原文:[https://www . geesforgeks . org/D3-js-band-band-function/](https://www.geeksforgeeks.org/d3-js-band-bandwidth-function/)

d3.js 中的 **band.bandwidth()函数**用来求每个波段的宽度。

**语法:**

```
band.bandwidth()
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回每个波段的宽度。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang = "en">

<head>
    <meta charset = "UTF-8" />
    <meta name = "viewport"
        path1tent = "width=device-width,
        initial-scale = 1.0"/>
    <script src =
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>
        // Creating the band scale with
        // specified domain and range.
        var A = d3.scaleBand()
                    .domain([10, 20, 30, 40, 50])
                    .range([0, 10]);

        // Applying bandwidth() Function
        let gfg = A.bandwidth();

        // Printing the Output 
        console.log("Bandwidth Of A: ",gfg);

    </script>
</body>

</html>
```

**输出:**

```
Bandwidth Of A:  2
```

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang = "en">

<head>
    <meta charset = "UTF-8" />
    <meta name = "viewport"
        path1tent = "width=device-width,
        initial-scale = 1.0"/>
    <script src =
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>
        // Creating the band scale with
        // specified domain and range.
        var B = d3.scaleBand()
                    .domain(["one", "two", "three", "four"])
                    .range([0, 60]);

        // Applying bandwidth() Function
        let gfg = B.bandwidth();

        // Printing the Output 
        console.log("Bandwidth Of each band in B: ",gfg);
    </script>
</body>

</html>
```

**输出:**

```
Bandwidth Of each band in B:  15
```