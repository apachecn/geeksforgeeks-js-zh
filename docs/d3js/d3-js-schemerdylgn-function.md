# D3.js schemeRdYlGn【】功能

> 原文:[https://www.geeksforgeeks.org/d3-js-schemerdylgn-function/](https://www.geeksforgeeks.org/d3-js-schemerdylgn-function/)

D3.js 中的 **d3.schemeRdYlGn[]** 函数用于从 RdYlGn 顺序配色方案中返回特定的颜色，该配色方案以十六进制字符串的形式返回。

**语法:**

```
d3.schemeRdYlGn[k]
```

**参数:**该函数接受如上所述的单个参数，描述如下:

*   [T0】 k: “k "K" is a number.

**返回值:**返回一个十六进制字符串。

下面是上面给出的函数的几个例子。

**范例 1:**

```
<!DOCTYPE html> 
<html lang="en"> 
<head> 
    <meta charset="UTF-8" /> 
    <meta name="viewport"
        path1tent="width=device-width,  
        initial-scale=1.0"/> 

    <title>D3.js schemeRdYlGn[] Function</title> 
    <script src= "https://d3js.org/d3.v4.min.js"></script> 
    <script src= "https://d3js.org/d3-color.v1.min.js"></script> 
    <script src= "https://d3js.org/d3-interpolate.v1.min.js"></script> 
    <script src= "https://d3js.org/d3-scale-chromatic.v1.min.js"></script> 
</head> 
<body> 
    <center>
    <h1 style="color:green;">GeeksForGeeks</h1>

    <h3>D3.js schemeRdYlGn[] Function</h3>

    <script> 
        document.write(d3.schemeRdYlGn[6][0]+"<br>"); 
        document.write(d3.schemeRdYlGn[6][1]+"<br>");
        document.write(d3.schemeRdYlGn[6][2]+"<br>");
        document.write(d3.schemeRdYlGn[6][3]+"<br>");
        document.write(d3.schemeRdYlGn[6][4]+"<br>");
        document.write(d3.schemeRdYlGn[6][5]);
    </script> 
    </center>
</body> 
</html>
```