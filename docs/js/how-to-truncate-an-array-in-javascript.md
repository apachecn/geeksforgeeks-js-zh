# 如何在 JavaScript 中截断数组？

> 原文:[https://www . geesforgeks . org/如何截断 javascript 中的数组/](https://www.geeksforgeeks.org/how-to-truncate-an-array-in-javascript/)

在 JavaScript 中，有两种截断数组的方法。一种是使用 length 属性，另一种是使用 splice()方法。在本文中，我们将看到如何使用这两种方法在 JavaScript 中截断数组。

1.  [length](https://www.geeksforgeeks.org/javascript-array-length-property/) attribute

[拼接()](https://www.geeksforgeeks.org/javascript-array-splice-method/)

**使用 array.length 属性:**使用 array.length 属性，可以改变数组的长度。它可以帮助您决定数组元素在输出中出现的长度。

**语法:**

```
// n = number of elements you want to print
var_name.length = n;
```

在上面的语法中，您可以根据所需的输出，使用 array.length 属性为数组分配大小。

**例:**

## Javascript

```
<script>
  const num = [1, 2, 3, 4, 5, 6];
  num.length = 3;
  console.log( num );
</script>
```

**输出:**

```
[1, 2, 3]
```

正如您在上面的输出中看到的，只有三个元素被打印出来。将值赋给 array.length 属性会截断数组，并且在程序之后只存在前 n 个值。

**使用 splice()方法:**splice()方法从数组中移除项，并返回移除的项。

**语法:**

```
// n=number of elements you want to print
var_name.splice(n); 
```

**例:**

## Javascript

```
<script>
  const num = [1, 2, 3, 4, 5, 6];
  num.splice(4);
  console.log(num);
</script>
```

**输出:**

```
[1, 2, 3, 4]
```

以上是在 JavaScript 中截断数组的两种方法。