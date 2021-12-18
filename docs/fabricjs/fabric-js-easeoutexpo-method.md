# Fabric.js easeOutExpo()方法

> 原文:[https://www.geeksforgeeks.org/fabric-js-easeoutexpo-method/](https://www.geeksforgeeks.org/fabric-js-easeoutexpo-method/)

在动画和游戏中，可以看到许多物体从一个点线性移动到另一个点。但是在使用“放松”功能后，对象的前进方式可以呈现出不同的自然和有趣的形状。

**缓和函数**是参数随时间的变化率。就是那种开始时运动缓慢，结束时加速、减速的方程。这组方程取自罗伯特·彭纳的书和网页。

**easeOutExpo()方法**用于指数缓和。

**语法:**

```
easeOutExpo(t, b, c, d)
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

 // Initializing easeOutExpo() function
 function easeOutExpo (t, b, c, d) {
    return (t == d) ? b + c : c * (-Math.pow(2, -10 * t / d) + 1) + b;
 }

 // Calling the easeOutExpo() function over
 // the specified parameter values
 console.log(fabric.util.ease.easeOutExpo(1, 2, 3, 4)); 
</script>

</body>

</html>
```

**输出:**

```
4.4696699141100895
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

 // Initializing easeOutExpo() function
 function easeOutExpo (t, b, c, d) {
    return (t == d) ? b + c : c * (-Math.pow(2, -10 * t / d) + 1) + b;
 }

 // Initializing the parameters with its values
 var t = 5;
 var b = 10;
 var c = 40;
 var d = 12;

 // Calling the easeOutExpo() function over
 // the specified parameter values
 console.log(fabric.util.ease.easeOutExpo(t, b, c, d)); 
</script>

</body>

</html>
```

**输出:**

```
47.772753204649156
```