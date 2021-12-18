# JavaScript Date todaytestring()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-todaytestring-method/](https://www.geeksforgeeks.org/javascript-date-todatestring-method/)

下面是**Date todaytestring()**方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 15, 1996 05:35:32');

       // Contents of date portion of above date
       // object is converted into a string using
       // toDateString() method.
       var B = dateobj.toDateString();

       // Printing the converted string.
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    Tue Oct 15 1996
    ```

**date . todaytestring()**方法用于将给定日期对象的日期部分内容转换为字符串。日期对象是使用 date()构造函数创建的。

**语法:**

```
dateObj.toDateString()
```

**参数:**此方法不接受任何参数。它只是与使用 Date()构造函数创建的 Date 对象一起使用。

**返回值:**返回转换后的 Date()构造函数内容的日期部分的字符串。

**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，其日期部分的内容被转换为字符串。

以上方法的更多代码如下:
**程序 1:** 这里在创建日期对象时没有传递任何参数，但是 toDateString()方法返回当前的日名、月名、日期、年。

```
<script>
  // Here nothing has been assigned
  // while creating Date object
  var dateobj = new Date();

   // Contents of date portion of above date
   // object is converted into a string using
   // toDateString() method.
   var B = dateobj.toDateString();

   // Printing the converted string.
   document.write(B);
</script>
```

**输出:**

```
Mon Apr 23 2018
```

**程序 2:** 当一些随机的值列表被传递时，toDateString()方法返回相应的生成字符串。

Date()构造函数的格式类似于 Date(月、日、年、时)。按照这种格式，在下面的程序中给出了一些值，并产生相应的字符串作为输出。时间格式应该像(数:数:数)。如果时间不是这种格式，它将输出无效日期。

```
<script>
   // Here some different values has been
   // assigned while creating Date object
   var dateobj1 = new Date('1');
   var dateobj2 = new Date('2, 3');
   var dateobj3 = new Date('4, 5, 6');
   var dateobj4 = new Date('7, 8, 3, 4');
   var dateobj5 = new Date('4, 5, 6, 11:00:12');
   var dateobj6 = new Date('12, 5, 4, 0:0');

   // Contents of date portion of above date
   // object is converted into a string using
   // toDateString() method.
   var B = dateobj1.toDateString();
   var C = dateobj2.toDateString();
   var D = dateobj3.toDateString();
   var E = dateobj4.toDateString();
   var F = dateobj5.toDateString();
   var G = dateobj6.toDateString();

  // Printing the converted string.
  document.write(B + "<br />");
  document.write(C + "<br />");
  document.write(D + "<br />");
  document.write(E + "<br />");
  document.write(F + "<br />");
  document.write(G);
</script>
```

**输出:**

```
Mon Jan 01 2001
Sat Feb 03 2001
Wed Apr 05 2006
Invalid Date
Wed Apr 05 2006
Sun Dec 05 2004
```

**程序 3:** 月、日期、小时、分钟、秒和毫秒应该在它们各自的范围内，月为 0 到 11，日期为 1 到 31，小时为 0 到 23，分钟为 0 到 59，秒为 0 到 59，毫秒为 0 到 999，否则 toDateString()方法返回无效日期。
此处给出的日期为 45，超出了日期范围，这就是为什么下面的代码给出的输出为空。

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = 
  new Date('October 45, 1996 05:35:32');

   // Contents of date portion of above date
   // object is converted into a string using
   // toDateString() method.
   var B = dateobj.toDateString();

   // Printing the converted string.
   document.write(B);
</script>
```

**输出:**

```
Invalid Date
```

**支持的浏览器:**JavaScript Date todaytestring()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 5 及以上
*   Safari 1 及以上