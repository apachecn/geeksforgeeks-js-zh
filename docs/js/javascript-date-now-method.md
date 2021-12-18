# JavaScript Date now()方法

> 原文:[https://www.geeksforgeeks.org/javascript-date-now-method/](https://www.geeksforgeeks.org/javascript-date-now-method/)

在本文中，我们将学习 Javascript 中的 Date now()方法。 **date.now()** 方法用于返回自 1970 年 1 月 1 日 00:00:00 UTC 以来经过的毫秒数。由于 now()是一个静态的 Date 方法，所以它将始终用作 Date.now()。

**语法:**

```
var A = Date.now();
```

**参数:**此方法不接受任何参数。

**返回值:**返回自 1970 年 1 月 1 日 00:00:00 UTC 以来经过的毫秒数。

其他日期方法详见 [JavaScript 获取日期方法](https://www.geeksforgeeks.org/javascript-get-date-methods/)一文。

上述方法的更多代码如下:

**示例 1:** 以下示例说明了 **Date now()** 方法。

## java 描述语言

```
<script>

  // Use of method Date.now()
  var A = Date.now();

  // Printing the number of millisecond elapsed
  document.write("The time elapsed in millisecond is: " + A);
</script>
```

**输出:**

```
The time elapsed in millisecond is: 1529644667834
```

**示例 2:** 本示例说明了使用 **Date.now()** 方法获取当前日期。

## java 描述语言

```
<script>

  // Use of Date.now() method
  var d = Date(Date.now());

  // Converting the number of millisecond
  // in date string
  a = d.toString()

  // Printing the current date                   
  document.write("The current date is: " + a)
</script>
```

**输出:**

```
The current date is: Fri Jun 22 2018 10:54:33 
GMT+0530 (India Standard Time)
```

**示例 3:**Date(Date . now())与 Date()相同，因此可以使用以下代码获得相同的结果，即当前日期。

## java 描述语言

```
<script>
  // Using Date() method
  var d = Date();

  // Converting the number value to string
  a = d.toString()

  // Printing the current date
  document.write("The current date is: " + a)
</script>
```

**输出:**

```
The current date is: Fri Jun 22 2018 11:02:01 
GMT+0530 (India Standard Time)
```

**支持的浏览器:**下面列出了 **JavaScript Date now()方法**支持的浏览器:

*   谷歌 Chrome 5 及以上版本
*   微软 Edge 12 及以上版本
*   Firefox 3 及以上版本
*   Internet Explorer 9 及以上版本
*   Opera 10.5 及以上
*   Safari 4 及以上