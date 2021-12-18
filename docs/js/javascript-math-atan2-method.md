# JavaScript 数学 atan2()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-atan2-method/](https://www.geeksforgeeks.org/javascript-math-atan2-method/)

下面是方法的例子。

*   **Example:** When the Y coordinate is greater than the X coordinate:

## Javascript

```
<script type="text/javascript">
       document.write(Math.atan2(90, 15)); 
</script>
```

**输出:**

```
1.4056476493802699

```

**Math.atan2()** 方法用于返回其参数商的反正切。Math.atan2()方法返回一个介于-π和π之间的数值，表示(x，y)点与正 x 轴的角度θ。这是正 X 轴和点(X，y)之间的逆时针角度，单位为弧度。

**语法:**

```
Math.atan2(value1, value2)

```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **Value 1:** This parameter represents the Y coordinate.
*   **Value 2:** indicates the x coordinate of the point (x, y).

**返回:**返回其参数商的反正切。

以下示例说明了 JavaScript 中的 Math.atan2()方法:

*   **Example 1:**

```
Input : Math.atan2(90, 15);  
Output : 1.4056476493802699

```

*   **Example 2:**

```
Input : Math.atan2(15, 90);
Output : 0.16514867741462683

```

上述方法的更多代码如下:

**程序 1:** 当 y 坐标小于 x 坐标时

## Javascript

```
<script type="text/javascript">
     document.write(Math.atan2(15, 90)); 
</script>
```

**输出:**

```
0.16514867741462683

```

**程序二:**当 y 坐标与 x 坐标相同时

## Javascript

```
<script type="text/javascript">
     document.write(Math.atan2(90, 90)); 
</script>
```

**输出:**

```
0.7853981633974483

```

**支持的浏览器:**

*   谷歌铬
*   Internet browser
*   red fox
*   歌剧
*   旅行队