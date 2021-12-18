# JavaScript Date getutcmails()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getutcmails-method/](https://www.geeksforgeeks.org/javascript-date-getutcmilliseconds-method/)

下面是**Date getutcmails()**方法的例子。

*   **示例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 15, 1996 05:35:32:77 GMT+11:00');

   // millisecond from above date object is
   // being extracted using getUTCMilliseconds().
   var B = dateobj.getUTCMilliseconds();

   // Printing millisecond according
   // to universal time
   document.write(B);
</script>
```

*   **输出:**

```
77
```

**date . getutcmails()**方法用于根据通用时间从给定的 Date 对象中获取毫秒。
**语法:**

```
DateObj.getUTCMilliseconds();
```

**参数:**此方法不接受任何参数。它只是与一个日期对象一起使用，我们希望根据世界时间从该日期对象中获取毫秒。

**返回值:**根据世界时返回给定日期对象的毫秒数。毫秒是介于 0 到 999 之间的整数值。

**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，我们希望根据世界时从该对象中获取毫秒。

上述方法的更多代码如下:

**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是一个数字，因为月份的日期不存在。如果月份的日期不存在，根据世界时，毫秒将不存在。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object.
   var dateobj =
   new Date('October 33, 1996 05:35:32:77 GMT+11:00');

   // millisecond from above date object is
   // being extracted using getUTCMilliseconds().
   var B = dateobj.getUTCMilliseconds();

   // Printing millisecond according
   // to universal time.
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果在创建 Date 对象时没有给 Date()构造函数毫秒，getutcmails()方法根据世界时返回零(0)。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32 GMT+11:00');

   // millisecond from above date object is
   // being extracted using getUTCMilliseconds().
   var B = dateobj.getUTCMilliseconds();

   // Printing millisecond according
   // to universal time.
   document.write(B);
</script>
```

**输出:**

```
0
```

**程序 3:** 如果在创建 Date 对象时没有给 Date()构造函数任何参数，getutcmails()方法将根据世界时返回当前毫秒。

## java 描述语言

```
<script>
   // creating Date object
   var dateobj = new Date();

   // millisecond from above date object is
   // being extracted using getUTCMilliseconds().
   var B = dateobj.getUTCMilliseconds();

   // Printing current millisecond
   // according to universal time.
   document.write(B);
</script>
```

**输出:**

```
566
```

**程序 4:** 如果在创建 Date 对象时给了 Date()构造函数范围[0，999]之外的毫秒，getutcmails()方法将返回 0 作为异常，因为毫秒范围在 0 到 999 之间，1003 超出了该范围。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32:1003 GMT+11:00');

   // millisecond from above date object is
   // being extracted using getUTCMilliseconds().
   var B = dateobj.getUTCMilliseconds();

   // Printing millisecond
   // according to universal time.
   document.write(B);
</script>
```

**输出:**

```
0
```

**支持的浏览器:**下面列出了**JavaScript Date getutcmails()方法**支持的浏览器:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上