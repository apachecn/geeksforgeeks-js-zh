# D3.js log.range()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-log-range-function/](https://www.geeksforgeeks.org/d3-js-log-range-function/)

**log.range()** 函数将对数刻度的范围设置为必须包含两个或两个以上值的指定值数组。范围内的元素可以是数字或字符串。

**语法:**

```
log.range([range]);
```

**参数:**该函数采用上面给出并在下面描述的单个参数。

*   **【范围】:**包含指定域范围的数组。

**返回值:**该函数不返回值。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" path1tent="width=device-width, 
                   initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>
        var log = d3.scaleLog()

            // Setting the domain for the scale.
            .domain([1, +10])

            // Setting the range for the scale
            .range([1, 2, 3, 4, 5]);
        console.log(log(1));
        console.log(log(10));
    </script>
</body>

</html>
```

**输出:**

```
1 
2
```

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" path1tent=
        "width=device-width,initial-scale=1.0" />
    <script src="https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>
        var log = d3.scaleLog()

            // Setting the domain for the scale
            .domain([10, 20])

            // Setting the range for the scale
            .range(["red", "green", "blue"]);
        console.log(log(10));
        console.log(log(15));
        console.log(log(20));
    </script>
</body>

</html>
```

**输出:**

```
rgb(255, 0, 0)
rgb(106, 75, 0)
rgb(0, 128, 0)

```