# JavaScript Date toJSON()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-to JSON-method/](https://www.geeksforgeeks.org/javascript-date-tojson-method/)

下面是 **Date toJSON()** 方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 15, 1996 05:35:32');

       // Contents of above date object is converted
       // into a string using toJSON() method.
       var B = dateobj.toJSON();

       // Printing the converted string.
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    1996-10-15T00:05:32.000Z
    ```

**date.toJSON()** 方法用于将给定日期对象的内容转换为字符串。日期对象是使用 date()构造函数创建的。
**语法:**

```
dateObj.toJSON()
```

**参数:**此方法不接受任何参数。它只是与使用 Date()constructor 创建的 Date 对象一起使用。

**返回值:**返回转换后的 Date()构造函数内容的字符串。

**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，其内容被转换为字符串。

上述方法的更多代码如下:

**程序 1:** 在这里，在创建日期对象时没有作为参数传递任何内容，但是 toJSON()方法返回当前的日名称、月名称、日期、年和时间。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // Contents of above date object is
   // converted into a string using toJSON() method.
   var B = dateobj.toJSON();

  // Printing the converted string.
  document.write(B);
</script>
```

**输出:**

```
2018-04-23T11:24:14.955Z
```

**程序 2 :** 当一些随机的值列表被传递时，那么 toJSON()方法返回相应的产生的字符串。
Date()构造函数的格式类似于 Date(月、日、年、时)。按照这种格式，在下面的程序中给出了一些值，并产生相应的字符串作为输出。时间格式应该像(数:数:数)。

```
<script>
   // Here some different values has been
   // assigned while creating Date object
   var dateobj1 = new Date('1');
   var dateobj2 = new Date('2, 3');
   var dateobj3 = new Date('4, 5, 6');
   var dateobj4 = new Date('4, 5, 6, 11:00:12');
   var dateobj5 = new Date('12, 5, 4, 0:0');

   // Contents of above date objects is converted
   // into strings using toJSON() method.
   var B = dateobj1.toJSON();
   var C = dateobj2.toJSON();
   var D = dateobj3.toJSON();
   var E = dateobj4.toJSON();
   var F = dateobj5.toJSON();

   // Printing the converted string.
   document.write(B + "<br>");
   document.write(C + "<br>");
   document.write(D + "<br>");
   document.write(E + "<br>");
   document.write(F);
</script>
```

**输出:**

```
2000-12-31T18:30:00.000Z
2001-02-02T18:30:00.000Z
2006-04-04T18:30:00.000Z
2006-04-05T05:30:12.000Z
2004-12-04T18:30:00.000Z
```

**注意:**月、日期、小时、分钟、秒和毫秒必须在各自的范围内，月为 0 到 11，日期为 1 到 31，小时为 0 到 23，分钟为 0 到 59，秒为 0 到 59，毫秒为 0 到 999，否则 toJSON()方法**返回 null** 。

**程序 3:** 此处给出的日期为 45，超出了日期范围，这就是为什么下面的代码给出的输出为空。

```
<script>
   // Here a date has been assigned
   // while creating a Date object
   var dateobj = 
   new Date('October 45, 1996 05:35:32');

   // Contents of above date object is converted
   // into a string using toJSON() method.
   var B = dateobj.toJSON();

   // Printing the converted string.
   document.write(B);
</script>
```

**输出:**

```
null
```

**支持的浏览器:**JavaScript Date to JSON()方法支持的浏览器如下:

*   谷歌 Chrome 3 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 8 及更高版本
*   Opera 10.5 及以上
*   Safari 5 及以上