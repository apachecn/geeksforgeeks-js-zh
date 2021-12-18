# fabric . js get random nt()方法

> 原文:[https://www . geesforgeks . org/fabric-js-get random nt-method/](https://www.geeksforgeeks.org/fabric-js-getrandomint-method/)

**getRandomInt()方法**用于返回两个指定数字之间的随机数。

**语法:**

```
getRandomInt(min, max)
```

**参数:**该方法接受两个参数，如上所述，如下所述:

*   **分钟:**该参数保持指定的下限值。
*   **最大值:**该参数保持指定的上限值。

**返回值:**该方法返回最小值和最大值之间的随机数(包括)。每次运行输入文件时，输出都会改变。

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

      // Calling getRandomInt() function over
      // some specified min and max values
      console.log(fabric.util.getRandomInt(1, 1));
      console.log(fabric.util.getRandomInt(1, 2));
      console.log(fabric.util.getRandomInt(1, 4));
      console.log(fabric.util.getRandomInt(2, 10));
    </script>
  </body>

</html>
```

**输出:**

```
1
2
2
8
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

      // Specifying some min and max values
       var min1 = 1;
       var max1 = 4;
       var min2 = 12;
       var max2 = 20;

      // Calling getRandomInt() function over
      // the above specified min and max values
      console.log(fabric.util.getRandomInt(min1, max1));
      console.log(fabric.util.getRandomInt(min2, max2));
    </script>
  </body>

</html>
```

**输出:**

```
2
19
```