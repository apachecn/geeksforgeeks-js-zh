# JavaScript 日期 getMonth()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-get month-method/](https://www.geeksforgeeks.org/javascript-date-getmonth-method/)

下面是 **Date getMonth()** 方法的例子。

*   **例:**

## java 描述语言

```
<script type="text/javascript">
   // Creating a Date Object
   var DateObj = new Date('October 15, 1996 05:35:32');

   // Month from above Date Object is
   // Being extracted using getMonth()
   var months = DateObj.getMonth();

   // Printing month.
   document.write(months);
</script>
```

*   **输出:**

```
9
```

**date.getMonth()** 方法用于从给定的 date 对象中获取月份(0 到 11)。
**语法:**

```
DateObj.getMonth()
```

**参数:**本功能不接受任何参数。
**返回值:**返回给定日期对象的月份。月份是一个从 0 到 11 的整数值。零(0)表示 1 月，1 表示 2 月，以此类推，直到 11 日表示 12 月。
以上方法的更多代码如下:
**程序 1:** 这里月份的日期应该在 1 到 31 之间，因为没有日期可以有大于 31 的月份。这就是为什么如果 Date 对象中的月份大于 31，它会返回 NaN，即 Not Number。

## java 描述语言

```
<script type="text/javascript">
   // Creating a Date Object
   var DateObj = new Date('October 33, 1996 05:35:32');

   // Month from above Date Object is being
   // Extracted using getMonth()
   var months = DateObj.getMonth();

   // Printing month.
   document.write(months);
</script>
```

**输出:**

```
NaN
```

**程序 2:** 如果没有给出月份，则返回零(0)。

## java 描述语言

```
<script type="text/javascript">
   // Creating a Date Object
   var DateObj = new Date('1996 05:35:32');

   // Month from above Date Object is being
   // Extracted using getMonth()
   var months = DateObj.getMonth();

   // Printing month.
   document.write(months);
</script>
```

**输出:**

```
0
```

**程序 3:** 如果没有给定参数，则返回当月。

## java 描述语言

```
<script type="text/javascript">
   // Creating a Date Object
   var DateObj = new Date();

   // Month from above Date Object is being
   // Extracted using getMonth()
   var months = DateObj.getMonth();

   // Printing month.
  document.write(months);
</script>
```

**输出:**

```
2
```

**支持的浏览器:****JavaScript Date getMonth()方法**支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上