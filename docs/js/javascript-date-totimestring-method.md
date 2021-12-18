# JavaScript Date toTimeString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-totimestring-method/](https://www.geeksforgeeks.org/javascript-date-totimestring-method/)

下面是 **Date toTimeString()** 方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 15, 1996 05:35:32');

       // Contents of above date object
       // of time portion is returned
       // using toTimeString() function.
       var B = dateobj.toTimeString();

       // Printing the time.
       document.write(B);
    </script>                    
    ```

*   **输出:**

    ```
    05:35:32 GMT+0530 (India Standard Time)
    ```

**date.toTimeString()** 方法用于返回给定日期对象的英文时间部分。日期对象是使用 date()构造函数创建的。

**语法:**

```
dateObj.toTimeString()
```

**参数:**此功能不接受任何参数。它只是与使用 Date()构造函数创建的 Date 对象一起使用，该构造函数的时间部分内容以类似英语的语言返回。

**返回值:**返回给定日期对象的时间部分的英文。

**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，其时间部分内容被返回。

上述方法的更多代码如下:

**程序 1:** 在这里，在创建日期对象时，没有作为参数传递任何东西，但 toTimeString()方法仍然返回当前时间。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // It return current time using 
   // toTimeString() method.
   var B = dateobj.toTimeString();

   // Printing the current time.
   document.write(B);
</script>
```

**输出:**

```
14:58:08 GMT+0530 (India Standard Time)
```

**程序 2:** 当 Date()构造函数的参数没有给出时间部分时，它将时间返回为零(0)。

```
<script>
   // Only month date and year are 
   // assigned without time while
   // creating Date object.
   var dateobj = new Date('October 15, 1996');

   // It returns time using 
   // toTimeString() method.
   var B = dateobj.toTimeString();

   // Printing the time.
   document.write(B);
</script>
```

**输出:**

```
00:00:00 GMT+0530 (India Standard Time)
```

**支持的浏览器:**JavaScript Date toTimeString()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 5 及以上
*   Safari 1 及以上