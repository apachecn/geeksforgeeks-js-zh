# Fabric.js easeOutElastic()方法

> 原文:[https://www . geesforgeks . org/fabric-js-easeoutelastic-method/](https://www.geeksforgeeks.org/fabric-js-easeoutelastic-method/)

在动画和游戏中，可以看到许多物体从一个点线性移动到另一个点。但是在使用“放松”功能后，对象的前进方式可以呈现出不同的自然和有趣的形状。

**缓和函数**是参数随时间的变化率。正是这类方程在开始时移动缓慢，在结束时加速和减速。这些方程组取自罗伯特·彭纳的书和网页。

**放松弹性()方法**用于弹性放松。

**语法:**

```
easeOutElastic(t, b, c, d)
```

**参数:**该方法接受四个参数，如上所述，如下所述:

*   **t:** 此参数保存动画开始的指定时间。例如，如果 t 的值为 0，则表示动画刚刚开始。
*   **b:** 此参数保存对象在 x 轴上的指定起始位置。例如，如果 b 的值为 10，则表示对象在 x 坐标上的起始位置为 10。
*   **c:** 此参数保存对象的指定值变化。例如，如果 c 的值是 30，这意味着对象必须向右移动 30°，以 40°结束。
*   **d:** 此参数保存整个过程的指定持续时间。例如，如果 d 的值为 2，则意味着对象有 2 秒的时间来执行从 10 到 40 的运动。

**返回值:**该方法返回物体的缓和位置，即物体在特定时间的位置。

**例 1:**

## 超文本标记语言

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

        // Initializing easeOutElastic() function
        function easeOutElastic (t, b, c, d) {
            var s = 1.70158;
            var p = 0;
            var a = c;
            if (t == 0) return b;
            if ((t /= d) == 1) return b + c;
            if (!p) p = d * .3;
            if (a < Math.abs(c)) {
              a = c;
              var s = p / 4;
            }
            else var s = p / (2 * Math.PI) * Math.asin(c / a);
            return a * Math.pow(2, -10 * t) * Math.sin((t * d - s) * 
              (2 * Math.PI) / p) + c + b;
        }

        // Calling the easeOutElastic() function over
        // the specified parameter values
        console.log(fabric.util.ease.easeOutElastic(1, 2, 3, 4)); 
    </script>

</body>

</html>
```

**输出:**

```
4.734834957055044
```

**例 2:**

## 超文本标记语言

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

        // Initializing easeOutElastic() function
        function easeOutElastic (t, b, c, d) {
            var s = 1.70158;
            var p = 0;
            var a = c;
            if (t == 0) return b;
            if ((t /= d) == 1) return b + c;
            if (!p) p = d * .3;
            if (a < Math.abs(c)) {
                a = c;
                var s = p / 4;
            }
            else var s = p / (2 * Math.PI) * Math.asin(c / a);
            return a * Math.pow(2, -10 * t) * Math.sin((t * d - s) * 
                        (2 * Math.PI) / p) + c + b;
        }

        // Initializing the parameters with its values
        var t = 5;
        var b = 10;
        var c = 40;
        var d = 12;

        // Calling the easeOutElastic() function over
        // the specified parameter values
        console.log(fabric.util.ease.easeOutElastic(t, b, c, d)); 
    </script>
</body>

</html>
```

**输出:**

```
51.70617003103307
```