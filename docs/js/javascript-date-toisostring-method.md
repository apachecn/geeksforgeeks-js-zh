# JavaScript Date to sostring()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-toisostring-method/](https://www.geeksforgeeks.org/javascript-date-toisostring-method/)

下面是**Date to sostring()**方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 15, 1996 05:35:32');

       // Contents of above date object is converted
       // into a string using toISOString() function.
       var B = dateobj.toISOString();

       // Printing the converted string.
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    1996-10-15T00:05:32.000Z
    ```

**date.toISOString()** 方法用于将给定日期对象的内容转换为 ISO 格式(ISO 8601)的字符串，即(YYYYY-MM-DDTHH:mm:ss.sssZ 或 YYYYYY-MM-DDTHH:mm:ss.sssZ)的形式。日期对象是使用 date()构造函数创建的。

**语法:**

```
dateObj.toISOString()
```

**参数:**该方法不取任何参数。它只是与使用 Date()构造函数创建的 Date 对象一起使用。

**返回值:**将日期()构造函数内容的转换字符串返回到国际标准化组织格式(ISO 8601)。

**注意:****日期对象**是使用日期()构造器创建的有效日期对象。
上述方法的更多代码如下:

**程序 1:** 在这里，在创建日期对象时，没有作为参数传递任何内容，但 toISOString()方法仍然返回当前的日名称、月名称、日期、年和时间。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // Contents of above date object is
   // converted into a string using toISOString() method.
   var B = dateobj.toISOString();

   // Printing the converted string.
   document.write(B);
</script>
```

**输出:**

```
2018-04-23T10:26:00.996Z
```

**程序 2:** 这里我们将传递一个日期对象给 toISOString()方法返回日名、月名、日期、年份和时间。

```
<script>
    // Here nothing has been assigned
    // while creating Date object
    var dateobj = 
    new Date('October 13, 1996 05:35:32 GMT-3:00');

    // Contents of above date object is
    // converted into a string using toISOString() method.
    var B = dateobj.toISOString();

    // Printing the converted string.
    document.write(B);
</script>                    
```

**输出:**

```
1996-10-13T08:35:32.000Z
```

**注意:**月、日、时、分、秒、毫秒都应该分别在 0 到 11、1 到 31、0 到 23、0 到 59、0 到 59、0 到 999 的范围内。

**支持的浏览器:**JavaScript Date to sostring()方法支持的浏览器如下:

*   谷歌 Chrome 3 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 9 及以上版本
*   Opera 10.5 及以上
*   Safari 5 及以上

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。