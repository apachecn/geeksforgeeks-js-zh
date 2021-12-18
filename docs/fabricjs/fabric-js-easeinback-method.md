# Fabric.js easeInBack()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-easeinback-method/](https://www.geeksforgeeks.org/fabric-js-easeinback-method/)

在游戏应用程序中，有许多以线性方式从 A 点到 B 点移动的对象，但是在应用了一个缓和之后，它可以使它看起来更自然。一个放松功能告诉动画它的进展。直线运动可以呈现有趣的形状。

**放松功能**是控制动画速度或指定参数随时间变化的速率，最终给出一些想要的效果的功能。这些方程导致开始时移动缓慢，接近结束时加速或减速。最常见的一组宽松方程式来自[罗伯特·彭纳的](http://robertpenner.com/easing/)网页。

**easeInBack()** 方法用于向后放松。

**语法:**

```
easeInBack(t, b, c, d)
```

**参数:**该方法接受四个参数，如上所述，如下所述。

*   **t:** 此参数保存动画开始的指定时间。例如，如果 t 的值为 0，则表示动画刚刚开始。
*   **b:** 此参数保存对象在 x 轴上的指定起始位置。例如，如果 b 的值为 10，则意味着对象在 x 坐标上的起始位置为 10。
*   **c:** 此参数保存对象值的指定变化。例如，如果 c 的值是 30，这意味着对象必须向右移动 30°，以 40°结束。
*   **d:** 此参数保存整个过程的指定持续时间。例如，如果 d 的值为 2，则意味着对象有 2 秒的时间来执行从 10 到 40 的这个运动。

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

  // Initializing easeInBack() function
  function easeInBack (t, b, c, d) {
    if (s == undefined) s = 1.70158;
    return c * (t /= d) * t * ((s + 1) * t - s) + b;
  }

  // Calling the easeInBack() function over 
  // the specified parameter values
  console.log(fabric.util.ease.easeInBack(1, 2, 3, 4));
</script>

</body>

</html>
```

**输出:**

```
1.8075903125
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

  // Initializing easeInBack() function
  function easeInBack (t, b, c, d) {
    if (s == undefined) s = 1.70158;
    return c * (t /= d) * t * ((s + 1) * t - s) + b;
  }

  // Initializing the parameters with its values
  var t = 5;
  var b = 10;
  var c = 40;
  var d = 12;

  // Calling the easeInBack() function over 
  // the specified parameter values
  console.log(fabric.util.ease.easeInBack(t, b, c, d));
</script>

</body>

</html>
```

**输出:**

```
6.000543981481481
```