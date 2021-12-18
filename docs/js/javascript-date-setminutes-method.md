# JavaScript 日期设置分钟()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-setminutes-method/](https://www.geeksforgeeks.org/javascript-date-setminutes-method/)

**date.setMinutes()** 方法用于将分钟设置到使用 date()构造函数创建的 Date 对象中。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32');

       // New minute of 52 is being set in above Date
       // Object with the help of setMinutes() function
       dateobj.setMinutes(52);

       // New minute from above Date Object is
       // being extracted using getMinutes()
       var B = dateobj.getMinutes();

       // Printing new minute
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    52
    ```

**语法:**

```
DateObj.setMinutes(Minutes_Value)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **分钟 _ 值:**此参数保存分钟值，用于在 Date()构造函数中设置。

**返回值:**返回用 setMinutes()方法设置的更新分钟的新日期。

**注意:****Date obj**是使用 Date()构造函数创建的有效日期对象，我们希望在其中设置分钟。分钟的值从 0 到 59。

上述方法的更多代码如下:

**程序 1:** 如果在 Date()构造函数中，我们在创建 Date 对象时没有给出任何分钟，setMinutes()方法仍然设置新的分钟，该分钟作为其参数给出。

```
<script>
   // Here minute has not been assigned
   // while creating Date object
   var dateobj = new Date('October 13, 1996');

   // new minute of 51 is being set in above Date
   // Object with the help of setMinutes() method
   dateobj.setMinutes(51);

   // new minute from above Date Object is
   // being extracted using getMinutes()
   var B = dateobj.getMinutes();

   // Printing new minute
   document.write(B);
</script>
```

**输出:**

```
51
```

**例 2:** 如果 Date()构造函数中没有给定参数，setMinutes()方法仍然设置分钟，但是月、年、日等变成当前的。这里 42 是新的分钟数，3 是当月即 4 月，1 是当前日期，2018 是当前年份。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // New minute of 42 is being set in above Date
   // Object with the help of setMinutes() method
   dateobj.setMinutes(42);

   // Minutes from above Date Object is
   // being extracted using getMinutes()
   var B = dateobj.getMinutes();

   // Month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Date from above Date Object is
   // being extracted using getDate()
   var D = dateobj.getDate();

   // Year from above Date Object is
   // being extracted using getFullYear()
   var E = dateobj.getFullYear();

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

**例 3:** 如果在 setMinutes()函数的参数中给定的分钟值是 66，它将设置 6 为分钟，因为分钟范围是从 0 到 59 和(66%60 = 6)。

这里 6 是新的分钟，小时从 05 变成 06，因为分钟的范围是从 0 到 59，即总计 60，我们将新的分钟设置为 66，它从 05 增加一小时到 06，分钟变成 6。

```
<script>
   // Here date has been assigned
   // while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32');

   // new minute of 66 is being set in above Date
   // Object with the help of setMinutes() function
   dateobj.setMinutes(66);

   // minute from above Date Object is
   // being extracted using getMinutes()
   var B = dateobj.getMinutes();

   // Hour from above Date Object is
   // being extracted using getHours()
   var C = dateobj.getHours();

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

**支持的浏览器:**JavaScript Date setMinutes()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上