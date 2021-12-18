# D3.js 插值维里迪斯()函数

> 原文:[https://www . geesforgeks . org/D3-js-interpreviridis-function/](https://www.geeksforgeeks.org/d3-js-interpolateviridis-function/)

D3.js 中的 **d3 .插值维里迪斯()**函数用于从“维里迪斯”顺序配色方案中返回特定的颜色，该配色方案以 RGB 字符串的形式返回。

**语法:**

```
d3.interpolateViridis(t)
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **[t:** "t" is a range of [0,1]

的数字

**返回值:**返回一个 RGB 字符串。

下面是上面给出的函数的几个例子。

**示例 1:**

```
<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8" /> 
    <meta name="viewport"
        path1tent="width=device-width,  
        initial-scale=1.0"/> 

    <title>D3.js interpolateViridis() Function</title> 
    <script src= "https://d3js.org/d3.v4.min.js"></script> 
    <script src= "https://d3js.org/d3-color.v1.min.js"></script> 
    <script src= "https://d3js.org/d3-interpolate.v1.min.js"></script> 
    <script src= "https://d3js.org/d3-scale-chromatic.v1.min.js"></script> 
</head> 
<body> 
    <center>
    <h1 style="color:green;">GeeksForGeeks</h1>

    <h3>D3.js interpolateViridis() Function</h3>

    <script> 
        document.write(d3.interpolateViridis(0)+"<br>"); 
        document.write(d3.interpolateViridis(0.1)+"<br>");
        document.write(d3.interpolateViridis(0.2)+"<br>");
        document.write(d3.interpolateViridis(0.3)+"<br>");
        document.write(d3.interpolateViridis(0.4)+"<br>");
        document.write(d3.interpolateViridis(0.5)+"<br>");
        document.write(d3.interpolateViridis(0.6)+"<br>");
        document.write(d3.interpolateViridis(0.7)+"<br>");
        document.write(d3.interpolateViridis(0.8)+"<br>");
        document.write(d3.interpolateViridis(0.9)+"<br>");
        document.write(d3.interpolateViridis(1));
    </script> 
    </center>
</body> 
</html>
```