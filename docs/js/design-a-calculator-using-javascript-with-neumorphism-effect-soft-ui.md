# 使用神经形态效果/软 UI 和 JavaScript 设计计算器

> 原文:[https://www . geesforgeks . org/design-a-calculator-using-JavaScript-with-neommorphism-effect-soft-ui/](https://www.geeksforgeeks.org/design-a-calculator-using-javascript-with-neumorphism-effect-soft-ui/)

在本文中，我们将学习如何使用 HTML、CSS 和 JavaScript 创建一个具有神经变形效果的工作计算器。使用这个计算器可以进行基本的数学运算，如加法、减法、乘法和除法。

**方法:**神经变形是当代装饰网页元素并在任何网页上创建 3D 效果的方法。HTML 和 CSS 可以用来创建这种动画效果。神经变形可以使用 CSS 盒子阴影特性来实现。它被用来给一个元素一个黑暗和光明的阴影。背景似乎与中性用户界面元素绑定在一起，就好像它们是从其中挤出来的或插入其中的一样。有人称之为“软用户界面”，因为软阴影是如何用来创造幻觉的，造型几乎是三维的。

**HTML 代码:**在本节中，我们将制作神经形态计算器的布局。

## 【index.html】

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta http-equiv="X-UA-Compatible" content="IE=edge">
    <meta name="viewport" content=
        "width=device-width, initial-scale=1.0">
    <title>Neumorphism Calculator</title>
    <link rel="stylesheet" href="style.css"> 
</head>

<body>
  <div class="container">
   <div class="cal-box">
    <form name="calculator">
      <input type="text" id="display" placeholder="0" readonly>
      <br>
      <input class="button" type="button" value="7" 
             onclick="calculator.display.value +='7'">
      <input class="button" type="button" value="8" 
             onclick="calculator.display.value +='8'">
      <input class="button" type="button" value="9" 
             onclick="calculator.display.value +='9'">
      <input class="button mathbutton" type="button" value="+" 
             onclick="calculator.display.value +='+'">
      <br>
      <input class="button" type="button" value="4" 
             onclick="calculator.display.value +='4'">
      <input class="button" type="button" value="5" 
             onclick="calculator.display.value +='5'">
      <input class="button" type="button" value="6" 
             onclick="calculator.display.value +='6'">
      <input class="button mathbutton" type="button" value="-"
             onclick="calculator.display.value +='-'">
      <br>
      <input class="button" type="button" value="1" 
             onclick="calculator.display.value +='1'">
      <input class="button" type="button" value="2" 
             onclick="calculator.display.value +='2'">
      <input class="button" type="button" value="3" 
             onclick="calculator.display.value +='3'">
      <input class="button mathbutton" type="button" value="x" 
             onclick="calculator.display.value +='*'">
      <br>
      <input class="button clearButton" type="button" value="C" 
             onclick="calculator.display.value =''">
      <input class="button" type="button" value="0" 
             onclick="calculator.display.value +='0'">
      <input class="button mathbutton" type="button" value="=" 
             onclick=
"calculator.display.value =eval(calculator.display.value)">

      <!-- eval() evaluates arithmetic expressions in display box -->
      <input class="button mathbutton" type="button" value="/" 
             onclick="calculator.display.value +='/'">
    </form>
   </div>
  </div>
</body>
</html>
```