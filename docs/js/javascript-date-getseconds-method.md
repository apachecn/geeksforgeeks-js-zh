# JavaScript 日期 getSeconds()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getseconds-method/](https://www.geeksforgeeks.org/javascript-date-getseconds-method/)

下面是 **Date getSeconds()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var DateObj = new Date('October 15, 1996 05:35:32');

  // second from above Date object is being
  // extracted using getSeconds()
  var sec = DateObj.getSeconds();

  // Printing second
  document.write(sec);
</script>
```

*   **输出:**

```
32
```

**date.getSeconds()** 方法用于从给定的 date 对象中获取秒。
**语法:**

```
DateObj.getSeconds()
```

**参数:**本功能不接受任何参数。
**返回值:**返回给定日期对象的第二个。秒是一个从 0 到 59 的整数值。
上述方法的更多代码如下:
**程序 1:** 这里月份的日期必须在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是一个数字，因为如果月份的日期不存在。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var DateObj = new Date('October 33, 1996 05:35:32');

  // second from above Date object is being
  // extracted using getSeconds()
  var sec = DateObj.getSeconds();

  // Printing second
  document.write(sec);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果没有给出秒，则返回零(0)。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var DateObj = new Date('October 13, 1996 05:35');

  // second from above Date object is being
  // extracted using getSeconds()
  var sec = DateObj.getSeconds();

  // Printing second
  document.write(sec);
</script>
```

**输出:**

```
0
```

**程序 3:** 如果没有给 Date()构造函数任何参数，则返回当前秒。

## java 描述语言

```
<script>
  // Creating a Date Object
  var DateObj = new Date();

  // second from above Date object is being
  // extracted using getSeconds()
  var sec = DateObj.getSeconds();

  // Printing second
  document.write(sec);
</script>
```

**输出:**

```
8
```

**程序 4:** 如果秒为 88，则作为异常返回 0，因为秒的范围在 0 到 59 之间，88 超出了这个范围。

## java 描述语言

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var DateObj = new Date('October 13, 1996 05:35:88');

  // second from above Date object is being
  // extracted using getSeconds()
  var sec = DateObj.getSeconds();

  // Printing second
  document.write(sec);
</script>
```

**输出:**

```
0
```

**支持的浏览器:**JavaScript Date getSeconds()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上