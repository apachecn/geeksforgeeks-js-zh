# JavaScript 日期设置小时()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-set hours-method/](https://www.geeksforgeeks.org/javascript-date-sethours-method/)

下面是 **Date setHours()** 方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32');

       // New hour 11 is being set in above Date
       // Object with the help of setHours() method
       dateobj.setHours(11);

       // New hour from above Date Object is
       // being extracted using getHours()
       var B = dateobj.getHours();

       // Printing new hour
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    11
    ```

**date.setHours()** 方法用于将小时设置到使用 date()构造函数创建的日期对象中。

**语法:**

```
DateObj.setHours(hours_Value)
```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **小时 _ 值:**该参数保存用于在 Date()构造函数中设置的小时值。

**返回值:**返回用 setHours()方法设置的更新小时的新日期。

**注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，我们希望在该构造函数中设置小时。

上述方法的更多代码如下:

**程序 1:** 如果在 Date()构造函数中，我们在创建 Date 对象时没有给出小时，那么 setHours()方法仍然会设置新的小时，该小时作为其参数给出。

```
<script>
   // Here hour has not been assigned
   // while creating Date object
   var dateobj = new Date('October 13, 1996');

   // New hour 11 is being set in above Date
   // Object with the help of setHours() method
   dateobj.setHours(11);

   // New hour from above Date Object is
   // being extracted using getHours()
   var B = dateobj.getHours();

   // Printing new hour
   document.write(B);
</script>
```

**输出:**

```
11
```

**例 2:** 如果 Date()构造函数中没有给定任何参数，仍然是 setHours()方法设置小时，但是月、年、日将是当前的月、年、日。这里 11 是新的小时，2 是当月即 3 月，30 是当前日期，2018 是当前年份。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = new Date();

   // new hour 11 is being set in above Date
   // Object with the help of setHours() method
   dateobj.setHours(11);

   // Hour from above Date Object is
   // being extracted using getHours()
   var B = dateobj.getHours();

   // Month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Date from above Date Object is
   // being extracted using getDate()
   var D = dateobj.getDate();

   // Year from above Date Object is
   // being extracted using getFullYear()
   var E = dateobj.getFullYear();

   // Printing new Hour
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
11
2
30
2018

```

**例 3:** 如果在 setHours()方法的参数中给出小时值为 26，它将设置 2 为小时，因为小时范围是从 0 到 23 和![26%24=2](img/baf4148c51ea461c67c4d7d464fb7bf7.png "Rendered by QuickLaTeX.com")。

这里 2 是新的小时，9 是月份，即 10 月，14 是日期，年份是 1996 年。这里我们看到 13 是原始日期，但是输出变成了 14，因为作为方法参数给出的 26 小时被转换为第二天的 2 小时，这就是为什么日期增加 1，即从 13 增加到 14。

```
<script>
   // Here nothing has been assigned
   // while creating Date object
   var dateobj = 
   new Date('October 13, 1996 05:35:32');

   // New hour 26 is being set in above Date
   // Object with the help of setHours() method
   dateobj.setHours(26);

   // Hour from above Date Object is
   // being extracted using getHours()
   var B = dateobj.getHours();

   // Month from above Date Object is
   // being extracted using getMonth()
   var C = dateobj.getMonth();

   // Date from above Date Object is
   // being extracted using getDate()
   var D = dateobj.getDate();

   // Year from above Date Object is
   // being extracted using getFullYear()
   var E = dateobj.getFullYear();

   // Printing new Hour
   document.write(B + "<br />");

   // Printing month
   document.write(C + "<br />");

   // Printing date
   document.write(D + "<br />");

   // Printing year
   document.write(E);
</script>
```

**输出:**

```
2
9
14
1996

```

**支持的浏览器:**JavaScript Date setHours()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 3 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上