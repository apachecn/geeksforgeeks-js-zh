# fabric . js easinoutcubic()方法

> 原文:[https://www . geesforgeks . org/fabric-js-easeinoutcubic-method/](https://www.geeksforgeeks.org/fabric-js-easeinoutcubic-method/)

在游戏或动画中，有许多移动对象可以以线性方式将它们从 A 点移动到 B 点，但是在应用了放松或放松功能后，它可以使其看起来更自然。一个放松功能说一个如何进步的动画。这样，直线运动可以呈现出有趣的形状。

**放松功能**指定参数随时间的变化率。正是他的方程式使某物在开始时缓慢移动，在接近结束时加速或减速。最常见的一组宽松方程式来自罗伯特·彭纳的书和网页。

**easeInOutCubic()方法**用于立方缓和进出。

**语法:**

```
easeInOutCubic(t, b, c, d)
```

**参数:**该方法接受上述和下述四个参数:

*   **t:** 此参数保存动画开始的指定时间。例如，如果 t 的值为 0，则表示动画刚刚开始。
*   **b:** 此参数保存对象在 x 轴上的指定起始位置。例如，如果 b 的值为 10，则表示对象在 x 坐标上的起始位置为 10。
*   **c:** 此参数保存对象的指定值变化。例如，如果 c 的值是 30，这意味着对象必须向右移动 30°，以 40°结束。
*   **d:** 此参数保存整个过程的指定持续时间。例如，如果 d 的值为 2，则意味着对象有 2 秒的时间来执行从 10 到 40 的运动。

**返回值:**该方法返回物体的缓和位置，即物体在特定时间的位置。

**例 1:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
  <!-- Adding the FabricJS library -->
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
  </script>
</head>

<body>
<script type="text/javascript">

 // Initializing easeInOutCubic() function
 function easeInOutCubic (t, b, c, d) {
    if ((t /= d / 2) < 1) return c / 2 * t * t * t + b;
    return c / 2 * ((t -= 2) * t * t + 2) + b;
 }

 // Calling the easeInOutCubic() function over
 // the specified parameter values
 console.log(fabric.util.ease.easeInOutCubic(1, 2, 3, 4)); 
</script>

</body>

</html>
```

**输出:**

```
2.1875
```

**例 2:**

## java 描述语言

```
<!DOCTYPE html>
<html>

<head>
  <!-- Adding the FabricJS library -->
  <script src=
"https://cdnjs.cloudflare.com/ajax/libs/fabric.js/3.6.2/fabric.min.js">
  </script>
</head>

<body>
<script type="text/javascript">

 // Initializing easeInOutCubic() function
 function easeInOutCubic (t, b, c, d) {
    if ((t /= d / 2) < 1) return c / 2 * t * t * t + b;
    return c / 2 * ((t -= 2) * t * t + 2) + b;
 }

 // Initializing the parameters with its values
 var t = 5;
 var b = 10;
 var c = 40;
 var d = 12;

 // Calling the easeInOutCubic() function over
 // the specified parameter values
 console.log(fabric.util.ease.easeInOutCubic(t, b, c, d)); 
</script>

</body>

</html>
```

**输出:**

```
21.574074074074076
```