# D3.js band.step()函数

> 原文:[https://www.geeksforgeeks.org/d3-js-band-step-function/](https://www.geeksforgeeks.org/d3-js-band-step-function/)

**d3.js** 中的 **band.step()** 函数用于查找通过查找相邻波段起点之间的距离而计算出的波段的步长。

**语法:**

```
band.step()
```

**参数:**此功能不接受任何参数。

**返回值:**该函数返回相邻波段起点之间的距离。

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
"https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>
        // Creating the band scale with 
        // specified domain and range
        var A = d3.scaleBand()
            .domain([10, 20, 30, 40, 50])
            .range([0, 10]);

        // Using the step() function
        let step_val = A.step();

        // Printing the Output  
        console.log("Step Of A: ", step_val);
    </script>
</body>

</html>
```

**输出:**

```
Step Of A:  2
```

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>

<head>
    <script src=
        "https://d3js.org/d3.v4.min.js">
    </script>
</head>

<body>
    <script>
        // Creating the band scale with 
        // specified domain and range
        var B = d3.scaleBand()
            .domain(["one", "two",
                "three", "four"])
            .range([0, 60]);

        // Using the step() function
        let step_val = B.step();

        // Printing the Output  
        console.log("Step in B: ", step_val);
    </script>
</body>

</html>
```

**输出:**

```
Step in B:  15

```