# JavaScript Date getutchows()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-date-getutc hours-method/](https://www.geeksforgeeks.org/javascript-date-getutchours-method/)

下面是**Date getutchows()**方法的例子。

*   **例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 15, 1996 23:35:32 GMT+11:00');

   // hour from above date object is being
   //  extracted using getUTCHours().
   var B = dateobj.getUTCHours();

   // Printing hour according to universal time.
   document.write(B);
</script>
```

*   **输出:**

```
12
```

**date . getutchlows()**方法用于根据通用时间从给定的 Date 对象中获取小时。
**语法:**

```
DateObj.getUTCHours();
```

**参数:**此方法不接受任何参数。它只是和一个日期对象一起使用，我们想从这个日期对象中根据世界时间获取小时。
**返回值:**根据世界时返回给定日期对象的小时数。Hours 是一个介于 0 到 23 之间的整数值。
**注意:****DateObj**是使用 Date()constructor 创建的有效日期对象，我们希望从该对象中根据世界时获取小时。
上述方法的更多代码如下:
**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是数字，因为月份的日期不存在。如果月份的日期不存在，根据世界时，小时将不存在。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 33, 1996 23:35:32 GMT+11:00');

   // Hour from above date object is
   // being extracted using getUTCHours().
   var B = dateobj.getUTCHours();

   // Printing hour according to universal time.
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果在创建 Date 对象时没有给出小时数，getUTCHours()方法会返回零(0)，但输出会打印为 13，因为根据世界时，0 表示为 13。这是个例外。

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 GMT+11:00');

   // Hour from above date object is
   // being extracted using getUTCHours().
   var B = dateobj.getUTCHours();

   // Printing hour according to universal time.
   document.write(B);
</script>
```

**输出:**

```
13
```

**程序 3:** 如果在创建 Date 对象时，没有给 Date()构造函数任何作为参数的内容，getUTCHours()方法将根据世界时返回当前小时。

## java 描述语言

```
<script>
   // creating Date Object
   var dateobj = new Date();

   // hour from above date object is
   // being extracted using getUTCHours().
   var B = dateobj.getUTCHours();

   // Printing current hour according
   // to universal time.
   document.write(B);
</script>
```

**输出:**

```
18
```

**支持的浏览器:**下面列出了**JavaScript Date getutchhours()方法**支持的浏览器:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上