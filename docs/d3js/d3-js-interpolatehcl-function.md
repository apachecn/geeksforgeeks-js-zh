# D3.js 插值 eHcl()函数

> 原文:[https://www . geesforgeks . org/D3-js-插值 ehcl-function/](https://www.geeksforgeeks.org/d3-js-interpolatehcl-function/)

D3.js 中的**插值 eHcl()** 函数用于返回两个颜色值之间的 CIELCh <sub>ab</sub> 颜色空间插值函数。给出的两种颜色是字符串格式，并使用 d3.hcl()函数转换为 CIELCh <sub>ab</sub> 格式。

**语法:**

```
d3.interpolateHcl(a, b);
```

**参数:**取以下两个参数。

*   **a:** 是弦。
*   **b:** 也是字符串。

**返回:**返回插值函数。

下面给出了上述函数的几个例子。

**示例 1:** 在控制台中。

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
  <!--fetching from CDN of D3.js -->
  <script type = "text/javascript"
          src = "https://d3js.org/d3.v4.min.js">
  </script>
  <script>
    // Printing the return type of the function
    console.log("Type of the function is: ",
 typeof(d3.interpolateHcl("green", "yellow")))
    // Using function d3.interpolateHcl()
    console.log("A RGB string: ",
 d3.interpolateHcl("green", "yellow")(0.5))
    console.log("A RGB string", 
d3.interpolateHcl("green", "white")(0.2))
  </script>
</body>
</html>
```

**输出:**

![](img/281c199e3c51e82ae13d4962ebdb0467.png)

**示例 2:** 在 HTML 中

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
  .box1, .box2{
    display: flex;
    margin-right: 40px;
    border-radius: 50% 50%;
    width: 150px;
    height: 150px;
  }
  div{
    display: flex;
  }
</style>
<body>
  D3.interpolateHcl()
  <div>
    <div class="box1">
    </div>
    <div class="box2">
    </div>
  </div>
  <!--fetching from CDN of D3.js -->
  <script type = "text/javascript" 
          src = "https://d3js.org/d3.v4.min.js">
  </script>
  <script>
    let box1=document.querySelector(".box1");
    let box2=document.querySelector(".box2");
    let color=d3.interpolateHcl("green", "yellow")(0.5);
    let color2=d3.interpolateHcl("green", "white")(0.2); 
    // Changing css of the div with class-name box1
    box1.style.backgroundColor=color;
    // Changing css of the div with class-name box2
    box2.style.backgroundColor=color2;
  </script>
</body>
</html>
```

**输出:**

![](img/94d6bf4d5b7612a346e72c8cf50c5e0d.png)