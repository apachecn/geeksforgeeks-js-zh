# D3.js 插值器()函数

> 原文:[https://www . geeksforgeeks . org/D3-js-interprecerens-function/](https://www.geeksforgeeks.org/d3-js-interpolategreens-function/)

d3.js 中的 **d3 .插值器()**功能用于返回“绿色”顺序配色对应的颜色。该功能用于返回不同深浅的绿色。

**语法:**

```
d3.interpolateGreens(t);
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **t:** 是 0 到 1 范围内的任意数字。

**返回值:**该函数返回一个 RGB 字符串。

下面是上面给出的函数的几个例子。

**例 1:**

```
<!DOCTYPE html> 
<html lang="en"> 
<head> 
<meta charset="UTF-8"> 
<meta name="viewport"
        content="width=device-width, 
                initial-scale=1.0"> 
<title>Document</title> 
</head> 
<style> 
</style> 
<body>
<!--Fetching from CDN of D3.js -->
  <script src = 
  "https://d3js.org/d3.v4.min.js"> 
  </script> 
  <script src=
  "https://d3js.org/d3-color.v1.min.js">
  </script>
  <script src=
  "https://d3js.org/d3-interpolate.v1.min.js">
  </script>
  <script src=
  "https://d3js.org/d3-scale-chromatic.v1.min.js">
  </script>
  <script> 
    console.log(d3.interpolateGreens(0));
    console.log(d3.interpolateGreens(0.4));
    console.log(d3.interpolateGreens(0.2));
    console.log(d3.interpolateGreens(0.25));
    console.log(d3.interpolateGreens(0.54));
    console.log(d3.interpolateGreens(0.85));
    console.log(d3.interpolateGreens(2));
    console.log(d3.interpolateGreens(1));
  </script> 
</body> 
</html>
```

**输出:**

![](img/5313dbe15a7113cade93eb0adb0a2e54.png)

**例 2:**

```
<!DOCTYPE html> 
<html lang="en"> 
<head> 
<meta charset="UTF-8"> 
<meta name="viewport"
        content="width=device-width, 
                initial-scale=1.0"> 
<title>Document</title> 
</head> 
<style> 
div{ 
  padding:6px;
  text-align: center;
  vertical-align: middle;
  display: flex;
  justify-content: center;
  width: 90px; 
  height: 50px; 
  float: left;
} 
</style> 
<body> 
  <h2>D3.interpolateGreens() </h2>
<div class="box1"> 
  <span>
  </span>
</div> 
<div class="box2"> 
  <span> 
  </span>
</div> 
<div class="box3"> 
  <span> 
  </span>
</div> 
<div class="box4"> 
  <span> 
  </span>
</div> 
<div class="box5"> 
  <span> 
  </span>
</div> 
<!--Fetching from CDN of D3.js -->
  <script src = 
  "https://d3js.org/d3.v4.min.js"> 
  </script> 
  <script src=
  "https://d3js.org/d3-color.v1.min.js">
  </script>
  <script src=
  "https://d3js.org/d3-interpolate.v1.min.js">
  </script>
  <script src=
  "https://d3js.org/d3-scale-chromatic.v1.min.js">
  </script>
  <script> 
    // creating different colors for different
    // Values of t as 0.1, 0.2...
    let color1= 
    d3.interpolateGreens(0.1); 
    let color2= 
    d3.interpolateGreens(0.2); 
      let color3= 
    d3.interpolateGreens(0.3); 
      let color4= 
    d3.interpolateGreens(0.4); 
      let color5= 
    d3.interpolateGreens(0.5);

    // Selecting Div using query selector
    let box1=document.querySelector(".box1"); 
    let box2=document.querySelector(".box2"); 
    let box3=document.querySelector(".box3"); 
    let box4=document.querySelector(".box4"); 
    let box5=document.querySelector(".box5"); 

    // Setting style and BG color of the particular DIVs
    box1.style.backgroundColor=color1; 
    box2.style.backgroundColor=color2; 
    box3.style.backgroundColor=color3; 
    box4.style.backgroundColor=color4; 
    box5.style.backgroundColor=color5; 
  </script> 
</body> 
</html>
```

**输出:**

![](img/5b4f9a64c61fbb478e838aa6e72a6b21.png)