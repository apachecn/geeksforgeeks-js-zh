# JavaScript 日期设置分钟()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-setutcments-method/](https://www.geeksforgeeks.org/javascript-date-setutcminutes-method/)

下面是**日期设置分钟()**方法的例子。

*   **例:**

## java 描述语言

```
<script>
   // Here a date has been assigned according to
   // universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32 GMT-3:00');

   // New minute of 52 is being set in above Date
   // Object with the help of setUTCMinutes() method
   dateobj.setUTCMinutes(52);

   // New minute from above Date Object is
   // being extracted using getUTCMinutes()
   var B = dateobj.getUTCMinutes();

   // Printing new minute
   document.write(B);
</script>
```

*   **输出:**

```
52
```

**date . setutctminutes()**方法用于根据通用时间将分钟设置到使用 Date()构造函数创建的日期对象中。
**语法:**

```
DateObj.setUTCMinutes(Minutes_Value);
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **分钟 _ 值:**此参数保存我们希望在使用 date()构造函数创建的日期中设置的分钟值。

**返回值:**返回新的即更新的分钟，该分钟由 setUTCMinutes()方法设置。
**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，我们希望在其中设置分钟。分钟的值从 0 到 59。
以上方法的更多代码如下:
**例 1:** 如果在 Date()构造函数中我们在创建 Date 对象时没有给出任何分钟，那么仍然 setUTCMinutes()方法将能够在创建的 Date 对象中根据世界时设置新的分钟。

## java 描述语言

```
<script>
   // Here minute has not been assigned according to
   // universal time while creating Date object
   var dateobj = new Date('October 13, 1996 GMT-3:00');

   // New minute of 51 is being set in above Date
   // Object with the help of setUTCMinutes() method
   dateobj.setUTCMinutes(51);

   // New minute from above Date Object is
   // being extracted using getUTCMinutes()
   var B = dateobj.getUTCMinutes();

   // Printing new minute
   document.write(B);
</script>
```

**输出:**

```
51
```

**例 2:** 如果在 Date()构造函数中没有给定任何参数，setUTCMinutes()方法仍然可以设置分钟，但是月、年、日期等仍然是当前的。
这里 42 是新分钟，3 是当月即 4 月，1 是当前日期，2018 是当前年份。

## java 描述语言

```
<script>
   // Here nothing has been assigned according to
   // universal time while creating Date object
   var dateobj = new Date();

   // New minute of 42 is being set in above Date
   // Object with the help of setUTCMinutes() method
   dateobj.setUTCMinutes(42);

   // Minutes from above Date Object is
   // being extracted using getUTCMinutes()
   var B = dateobj.getUTCMinutes();

   // Month from above Date Object is
   // being extracted using getUTCMonth()
   var C = dateobj.getUTCMonth();

   // Date from above Date Object is
   // being extracted using getUTCDate()
   var D = dateobj.getUTCDate();

   // Year from above Date Object is
   // being extracted using getUTCFullYear()
   var E = dateobj.getUTCFullYear();

   // Printing new minutes
   document.write(B + "<br />");

   // Printing current month
   document.write(C + "<br />");

   // Printing current date
   document.write(D + "<br />");

   // Printing current year
   document.write(E);
</script>
```

**输出:**

```
42
3
1
2018
```

**例 3:** 如果给定的分钟值为 66 作为 setUTCMinutes()方法的参数，它将设置 6 为分钟，因为分钟范围是 0 到 59，因此![66-60=6 ](img/ff8b0c54432ad816f2ec978aceea2fc6.png "Rendered by QuickLaTeX.com")，这里减去 60 是因为 0 到 59 是 60。

## java 描述语言

```
<script>
   // Here date has been assigned according to
   // universal time while creating Date object
   var dateobj =
   new Date('October 13, 1996 05:35:32 GMT-3:00');

   // New minute of 66 is being set in above Date
   // Object with the help of setUTCMinutes() method
   dateobj.setUTCMinutes(66);

   // Minute from above Date Object is
   // being extracted using getUTCMinutes()
   var B = dateobj.getUTCMinutes();

   // Hour from above Date Object is
   // being extracted using getUTCHours()
   var C = dateobj.getUTCHours();

   // Printing new minute
   document.write(B + "<br />");

   // Printing hour
   document.write(C);
</script>
```

**输出:**

```
6
6
```

**支持的浏览器:**JavaScript Date setutcments()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 4 及以上版本
*   歌剧 4 及以上
*   Safari 1 及以上