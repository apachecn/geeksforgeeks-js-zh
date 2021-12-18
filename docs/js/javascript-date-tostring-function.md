# JavaScript Date toString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-tostring-function/](https://www.geeksforgeeks.org/javascript-date-tostring-function/)

下面是 **Date toString()** 方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 15, 1996 05:35:32');

       // Contents of above date object is converted
       // into a string using toString() function.
       var B = dateobj.toString();

       // Printing the converted string.
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    Tue Oct 15 1996 05:35:32 GMT+0530 (India Standard Time)
    ```

**date.toString()** 方法用于将给定日期对象的内容转换为字符串。日期对象是使用 date()构造函数创建的。
**语法:**

```
dateObj.toString()
```

**参数:**此方法不接受任何参数。它只是与使用 Date()构造函数创建的 Date 对象一起使用，该构造函数的内容被转换为字符串。

**返回值:**返回转换后的字符串。

**注意:****DateObj**是一个使用 Date()constructor 创建的有效日期对象，其内容被转换为字符串。

以上方法的更多代码如下:
**程序 1:** 这里在创建日期对象时没有传递任何参数，但是 toString()方法返回当前的日名称、月名称、日期、年和时间。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // Contents of above date object
   // is converted into a string
   // using toString() method.
   var B = dateobj.toString();

   // Printing the converted string.
   document.write(B);
</script>                    
```

**输出:**

```
Wed Apr 11 2018 00:50:44 GMT+0530 (India Standard Time)
```

**程序 2:** 当一些随机的值列表被传递时，toString()方法返回相应的产生的字符串。

Date()构造函数的格式类似于 Date(月、日、年、时)。按照这种格式，在下面的程序中给出了一些值，并产生相应的字符串作为输出。时间格式应该类似于(数字:number:number)如果时间不在此格式中，它将输出无效日期。

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

   // Contents of above date objects is converted
   // into strings using toString() method.
   var B = dateobj1.toString();
   var C = dateobj2.toString();
   var D = dateobj3.toString();
   var E = dateobj4.toString();
   var F = dateobj5.toString();
   var G = dateobj6.toString();

   // Printing the converted string.
   document.write(B + "<br>");
   document.write(C + "<br>");
   document.write(D + "<br>");
   document.write(E + "<br>");
   document.write(F + "<br>");
    document.write(G);
</script>                    
```

**输出:**

```
Mon Jan 01 2001 00:00:00 GMT+0530 (India Standard Time)
Sat Feb 03 2001 00:00:00 GMT+0530 (India Standard Time)
Wed Apr 05 2006 00:00:00 GMT+0530 (India Standard Time)
Invalid Date"
Wed Apr 05 2006 11:00:12 GMT+0530 (India Standard Time)
Sun Dec 05 2004 00:00:00 GMT+0530 (India Standard Time)
```

**支持的浏览器:**JavaScript Date toString()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上