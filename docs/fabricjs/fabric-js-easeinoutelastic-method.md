# fabric . js easinoutelastic()方法

> 原文:[https://www . geesforgeks . org/fabric-js-easeinoutelastic-method/](https://www.geeksforgeeks.org/fabric-js-easeinoutelastic-method/)

在游戏或动画中，有许多移动对象可以将它们从 A 点线性移动到 B 点，但是在应用了放松或放松功能后，它可以使其看起来更加自然。一个放松功能说一个如何进步的动画。这样，直线运动可以呈现出有趣的形状。

**放松功能**指定参数随时间的变化率。正是他的方程式使某物在开始时缓慢移动，在接近结束时加速或减速。最常见的一组宽松方程式来自罗伯特·彭纳的书和网页。

**easinoutelastic()方法**用于缓和其所用对象的进出效果。

**语法:**

```
easeInOutElastic(t, b, c, d)
```

**参数:**该方法接受上述和下述四个参数:

*   **t:** 此参数保存动画开始的指定时间。例如，如果 t 的值为 0，则表示动画刚刚开始。
*   **b:** 此参数保存对象在 x 轴上的指定起始位置。例如，如果 b 的值为 10，则表示对象在 x 坐标上的起始位置为 10。
*   **c:** 此参数保存对象的指定值变化。例如，如果 c 的值是 30，这意味着对象必须向右移动 30°，以 40°结束。
*   **d:** 此参数保存整个过程的指定持续时间。例如，如果 d 的值为 2，则意味着对象有 2 秒的时间来执行从 10 到 40 的运动。

**返回值:**该方法返回物体的缓和位置，即物体在特定时间的位置。

**例 1:**

## 超文本标记语言

```
<html>
<head>
  <!-- Adding the FabricJS library -->
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
  </script>
</head>
<body>
<script type="text/javascript">

   // The easeInOutElastic() function
   function easeInOutElastic (t, b, c, d) {
      var s = 1.70158;
      var p = 0;
      var a = c;
      if (t == 0) return b;
      if ((t /= d / 2) == 2) return b + c;
      if (!p) p = d * (.3 * 1.5);
      if (a < Math.abs(c)) {
          a = c;
          var s = p / 4;
      }
      else var s = p / (2 * Math.PI) *
          Math.asin(c / a);
      if (t < 1) 
        return -.5 * (a *
             Math.pow(2, 10 * (t -= 1)) *
             Math.sin((t * d - s) *
                 (2 * Math.PI) / p)) + b;
      return a * Math.pow(2, -10 * (t -= 1)) *
        Math.sin((t * d - s)
          * (2 * Math.PI) / p) *
        .5 + c + b;
  }

   // Calling the easeInOutElastic() function
   // over the specified parameter values
   console.log(
     fabric.util.ease.easeInOutElastic(1, 2, 3, 4)
   ); 
</script>
</body>
</html>
```

**输出:**

```
2.0359083332712022
```

**例 2:**

## 超文本标记语言

```
<html>
<head>
  <!-- Adding the FabricJS library -->
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
  </script>
</head>
<body>
<script type="text/javascript">

   // Initializing the parameters
   // with its values
   var t = 5;
   var b = 10;
   var c = 40;
   var d = 12;

   // Calling the easeInOutElastic() function
   // over the specified parameter values
   console.log(
     fabric.util.ease.easeInOutElastic(t, b, c, d)
   ); 
</script>
</body>
</html>
```

**输出:**

```
5.676948575674239
```