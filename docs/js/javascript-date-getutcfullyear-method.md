# JavaScript Date getutcfyread()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-getutc full year-method/](https://www.geeksforgeeks.org/javascript-date-getutcfullyear-method/)

下面是 **Date getUTCFullYear()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 15, 1996 05:35:32 GMT+11:00');

   // year from above date object is
   // being extracted using getUTCFullYear().
   var B = dateobj.getUTCFullYear();

   // Printing year according to universal time.
   document.write(B);                   
</script>
```

*   **输出:**

```
1996
```

使用 **date.getUTCFullYear()** 方法从给定的 date 对象中根据世界时获取**年**。
**语法:**

```
DateObj.getUTCFullYear();
```

**参数:**该方法不取任何参数。它只是与一个日期对象一起使用，我们希望根据世界时从该日期对象中获取年份。
**返回值:**根据世界时返回给定日期对象**的年份。
**注意:****dateObj**是使用 Date()构造函数创建的有效日期对象，我们希望根据世界时从该对象中获取年份。
上述方法的更多代码如下:
**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回 NaN，即不是数字，因为月份的日期不存在。如果月份的日期不存在，年份也将不存在。** 

## java 描述语言

```
<script>
   // Here a date has been assigned according
   // to universal time while creating Date object
   var dateobj =
   new Date('October 45, 1996 05:35:32 GMT+11:00');

   // Year from above date object is
   // being extracted using getUTCFullYear().
   var B = dateobj.getUTCFullYear();

   // Printing year according to universal time.
   document.write(B);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果没有给 Date()构造函数任何参数，getUTCFullYear()函数根据世界时返回当前年份。

## java 描述语言

```
<script>
   // Creating Date object
   var dateobj = new Date();

   // Year from above date object is
   // being extracted using getUTCFullYear().
   var B = dateobj.getUTCFullYear();

   // Printing current year
   // according to universal time.
   document.write(B);
</script>
```

**输出:**

```
2018
```

**支持的浏览器:**支持的浏览器**JavaScript Date getutfullyear()方法**如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上