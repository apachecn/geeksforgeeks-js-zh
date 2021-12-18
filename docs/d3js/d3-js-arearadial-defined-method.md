# D3.js areaRadial.defined()方法

> 原文:[https://www . geesforgeks . org/D3-js-area radial-defined-method/](https://www.geeksforgeeks.org/d3-js-arearadial-defined-method/)

**D3 . js中的 **areaRadial.defined()** 方法可以指定是否为给定的数据点定义了数据。使用作为此方法的参数指定的布尔值或函数来检查每个点的值。如果此方法返回 true，则保留选中的值，否则忽略该值。**

**语法:**

```
areaRadial.defined( data_point )

```

**参数:** 该功能接受如上所述的单个参数，描述如下:

*   **data_point:** 是用于检查每个点的布尔值或函数。

**返回值:** 这个方法返回一个布尔值。

下面给出了 D3.js 中 **areaRadial.defined()** 方法的几个例子:

**例 1:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
  <script src=
"https://d3js.org/d3.v5.min.js">
  </script>
</head>
<body>
  <h1 style="text-align: center;
             color: green;">
    GeeksforGeeks
  </h1>
  <h3 style="text-align: center;">
    D3.js | areaRadial.defined() Method
  </h3>
  <center>
    <svg id="gfg" width="500" height="500">
      <g transform="translate(180,180)"></g>
    </svg>
  </center>
  <script>
    var data = [
      { x: 10, y: 1 },
      { x: 15, y: 3 },
      { x: 20, y: 5 },
      { x: 25, y: 7 },
      { x: 30, y: 9 },
      { x: 35, y: 11 },
      { x: 40, y: 13 }];

    var xScale = d3.scaleLinear()
        .domain([0, 8])
        .range([25, 200]);
    var yScale = d3.scaleLinear()
        .domain([0, 20])
        .range([200, 25]);

    var Gen = d3.areaRadial()
      .angle(d => xScale(d.x / 3))
      .innerRadius(d => yScale(d.y / 2))
      .outerRadius(d => yScale(d.y))
      // Omitting 4th index
      .defined((d, i) => (i != 4));

    d3.select("#gfg")
      .select("g")
      .append("path")
      .attr("d", Gen(data))
      .attr("fill", "green")
      .attr("stroke", "black");
  </script>
</body>
</html>
```

**输出:**

![](img/228dee84f87f3591ca99c8e5ce55459b.png)

**例 2:**

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
  <script src=
"https://d3js.org/d3.v5.min.js">
  </script>
</head>
<body>
  <h1 style="text-align: center;
             color: green;">
    GeeksforGeeks
  </h1>
  <h3 style="text-align: center;">
    D3.js | areaRadial.defined() Method
  </h3>
  <center>
    <svg id="gfg" width="200" height="200">
      <g transform="translate(100,100)"></g>
    </svg>
  </center>
  <script>
    var points = [
      { x: 0, y: 0 },
      { x: 2, y: 3 },
      { x: 4, y: 1 },
      { x: 6, y: 8 },
      { x: 8, y: 17 },
      { x: 10, y: 15 },
      { x: 12, y: 20 }];

    var xScale = d3.scaleLinear()
        .domain([0, 6])
        .range([0, 2 * Math.PI]);
    var yScale = d3.scaleLinear()
        .domain([0, 20])
        .range([90, 30]);

    var Gen = d3.areaRadial()
      .angle(d => xScale(d.x / 2))
      .innerRadius(d => yScale(d.y) / 2)
      .outerRadius(d => yScale(d.y))
      // Omitting 2nd index
      .defined((d, i) => (i != 2));

    d3.select("#gfg")
      .select("g")
      .append("path")
      .attr("d", Gen(points))
      .attr("fill", "green")
      .attr("stroke", "black");
  </script>
</body>
</html>
```

**输出:**

![](img/4337b044b563c1c3067836faeb2da293.png)