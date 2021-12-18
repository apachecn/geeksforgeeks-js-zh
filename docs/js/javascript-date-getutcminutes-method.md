# JavaScript Date getutchminutes()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getutchminutes-method/](https://www.geeksforgeeks.org/javascript-date-getutcminutes-method/)

下面是**Date getutcments()**方法的例子。

*   **例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dataobj =
   new Date('October 15, 1996 23:35:32 GMT+11:00');

  // Minute from above date object is
  // being extracted using getUTCMinutes().
  var B = dataobj.getUTCMinutes();

  // Printing minute according to universal time
  document.write(B);
</script>
```

*   **输出:**

```
35
```

**date . getutcments()**方法，用于根据通用时间从给定的 Date 对象中获取分钟。
**语法:**

```
DateObj.getUTCMinutes();
```

**参数:**此方法不接受任何参数。它只是和一个日期对象一起使用，我们想从中获取分钟数。
**返回值:**根据世界时返回给定日期的分钟数。分钟是一个从 0 到 59 的整数值。
**注意:**在上面的语法中， *DateObj* 是使用 Date()constructor 创建的有效日期对象，我们希望从中获取分钟。
上述方法的更多代码如下:
**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是数字，因为月份的日期不存在。如果月份日期不存在，根据世界时，分钟将不存在。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object.
   var dataobj =
   new Date('October 33, 1996 23:35:32 GMT+11:00');

   // Minute from above data object is
   // being extracted using getUTCMinutes().
   var B = dataobj.getUTCMinutes();

   // Printing minute according to universal time.
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果在创建 Date 对象时没有给 Date()构造函数分钟，那么 getUTCMinutes()方法根据世界时返回零(0)。这是个例外。

## java 描述语言

```
<script>
    // Here a date has been assigned according
    // to universal time while creating Date object.
    var dataobj =
    new Date('October 13, 1996 GMT+11:00');

    // Minute from above data object is
    // being extracted using getUTCMinutes().
    var B = dataobj.getUTCMinutes();

    // Printing minute according to
    // universal time.
    document.write(B);
</script>
```

**输出:**

```
0
```

**程序 3:** 如果在创建 Date 对象时没有给 Date()构造函数任何作为参数的内容，getUTCMinutes()方法将根据世界时返回当前分钟数。

## java 描述语言

```
<script>
   // Here nothing has been assigned according
   // to universal time while creating Date object.
   var dataobj = new Date();

   // Minute from above data object is
   // being extracted using getUTCMinutes().
   var B = dataobj.getUTCMinutes();

   // Printing current minute
   // according to universal time.
   document.write(B);
</script>
```

**输出:**

```
18
```

**支持的浏览器:**JavaScript Date getutcments()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上