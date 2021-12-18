# JavaScript 日期 toUTCString()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-toucstring-method/](https://www.geeksforgeeks.org/javascript-date-toutcstring-method/)

下面是**Date toutcsting()**方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = new Date('October 15, 1996 05:35:32');

       // Contents of above date object is converted
       // into a string using toUTCString() method.
       var B = dateobj.toUTCString();

       // Printing the converted string.
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    Tue, 15 Oct 1996 00:05:32 GMT
    ```

**date.toUTCString()** 方法用于根据世界时区 UTC 将给定日期对象的内容转换为字符串。日期对象是使用 date()构造函数创建的。

**语法:**

```
dateObj.toUTCString()
```

**参数:**此方法不接受任何参数。它只是与使用 Date()构造函数创建的 Date 对象一起使用，该构造函数的内容被转换为字符串。

**返回值:**根据世界时区 UTC 返回转换后的字符串。

**注意:****DateObj**是一个使用 Date()constructor 创建的有效日期对象，其内容被转换为字符串。

上述方法的更多代码如下:

**程序 1:** 这里在创建 date 对象的时候没有作为参数传递任何东西，但是 toUTCString()方法根据世界时区 UTC 返回当前的日名称、月名称、日期、年份和时间。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // Contents of above date object 
   // is converted into a string 
   // using toUTCString() method.
   var B = dateobj.toUTCString();

   // Printing the converted string.
   document.write(B);
</script>
```

**输出:**

```
Wed, 18 Apr 2018 08:30:48 GMT
```

**程序 2:** 当一些随机的值列表被传递时，toUTCString()方法返回相应的生成字符串。

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
   // into strings using toUTCString() method.
   var B = dateobj1.toUTCString();
   var C = dateobj2.toUTCString();
   var D = dateobj3.toUTCString();
   var E = dateobj4.toUTCString();
   var F = dateobj5.toUTCString();
   var G = dateobj6.toUTCString();

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
Sun, 31 Dec 2000 18:30:00 GMT
Fri, 02 Feb 2001 18:30:00 GMT
Tue, 04 Apr 2006 18:30:00 GMT
Invalid Date
Wed, 05 Apr 2006 05:30:12 GMT
Sat, 04 Dec 2004 18:30:00 GMT
```

**支持的浏览器:**以下列出了**JavaScript Date toutcsting()方法支持的浏览器:**

***   **谷歌 Chrome 1 哎亲 1997 年***   **edge12 and above***   **Firefox 1 哎亲 1997 年***   **互联网浏览器 4 及以上***   T21】Opera 4 and above**

**Safari 1**