# Fabric.js easeInOutQuint()方法

> 原文:[https://www . geesforgeks . org/fabric-js-easeinoutquint-method/](https://www.geeksforgeeks.org/fabric-js-easeinoutquint-method/)

在动画和游戏中，可以看到许多物体从一个点线性移动到另一个点。但是使用了 way 功能后，对象的前进方式可以呈现出不同的自然有趣的形状。

**缓和函数**是参数随时间的变化率。正是这类方程在开始时移动缓慢，在结束时加速、减速。这组方程取自罗伯特·彭纳的书和网页。

**easeInOutQuint()方法**用于五次进出缓和。

**语法:**

```
easeInOutQuint(t, b, c, d)
```

**参数:**该方法接受四个参数，如上所述，如下所述:

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

 // Initializing easeInOutQuint() function
 function easeInOutQuint (t, b, c, d) {
    if ((t /= d / 2) < 1) return c / 2 * t * t * t * t * t + b;
    return c / 2 * ((t -= 2) * t * t * t * t + 2) + b;
 }

 // Calling the easeInOutQuint() function over
 // the specified parameter values
 console.log(fabric.util.ease.easeInOutQuint(1, 2, 3, 4)); 
</script>

</body>

</html>
```

**输出:**

```
2.046875
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

 // Initializing easeInOutQuint() function
 function easeInOutQuint (t, b, c, d) {
    if ((t /= d / 2) < 1) return c / 2 * t * t * t * t * t + b;
    return c / 2 * ((t -= 2) * t * t * t * t + 2) + b;
 }

 // Initializing the parameters with its values
 var t = 5;
 var b = 10;
 var c = 40;
 var d = 12;

 // Calling the easeInOutQuint() function over
 // the specified parameter values
 console.log(fabric.util.ease.easeInOutQuint(t, b, c, d)); 
</script>

</body>

</html>
```

**输出:**

```
18.03755144032922
```