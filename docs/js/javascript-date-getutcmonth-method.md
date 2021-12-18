# JavaScript Date getutchmonth()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getutchmonth-method/](https://www.geeksforgeeks.org/javascript-date-getutcmonth-method/)

下面是**Date getutchmonth()**方法的例子。

**例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 15, 1996 23:35:32 GMT+11:00');

   // Month from above date object is
   // being extracted using getUTCMonth().
   var B = dateobj.getUTCMonth();

   // Printing month according
   // to universal time.
   document.write(B);
</script>
```

**输出:**

```
9
```

**date . getutchmonth()**方法，用于根据通用时间从给定的 Date 对象中获取月份。
**语法:**

```
DateObj.getUTCMonth();
```

**参数:**此方法不接受任何参数。它只是与我们想要从中提取月份的日期对象一起使用。
**返回值:**根据世界时返回给定日期对象的月份。月份是一个从 0 到 11 的整数值。零(0)表示 1 月，1 表示 2 月，以此类推，直到 11 日表示 12 月。
**注意:**在上面的语法中， **DateObj** 是一个使用 Date()constructor 创建的有效日期对象，我们要从中获取月份。
上述方法的更多代码如下:
**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是数字，因为月份的日期不存在。如果月份的日期不存在
，则根据世界时不存在月份

## java 描述语言

```
<script>
   // Here a date has been assigned according to
   // universal time while creating a Date object
   var dateobj =
   new Date('October 33, 1996 23:35:32 GMT+11:00');

   // Month from above date object is
   // being extracted using getUTCMonth().
   var B = dateobj.getUTCMonth();

   // Printing month according to universal time.
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果在创建 Date 对象时没有给 Date()构造函数一个月，那么 getUTCMonth()方法根据世界时返回零(0)。这是个例外。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj = new Date('1996 23:35:32 GMT+11:00');

   // Month from above date object is
   // being extracted using getUTCMonth().
   var B = dateobj.getUTCMonth();

   // Printing month according to universal time.
   document.write(B);
</script>
```

**输出:**

```
0
```

**程序 3:** 如果在创建 Date 对象时没有给 Date()构造函数任何参数，getUTCMonth()方法将根据世界时返回当前月份。

## java 描述语言

```
<script>
   // creating Date object
   var dateobj = new Date();

   // Month from above date object is
   // being extracted using getUTCMonth().
   var B = dateobj.getUTCMonth();

   // Printing current month
   // according to universal time.
   document.write(B);
</script>
```

**输出:**

```
2
```

**支持的浏览器:**T2 JavaScript Date getutchmonth()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上