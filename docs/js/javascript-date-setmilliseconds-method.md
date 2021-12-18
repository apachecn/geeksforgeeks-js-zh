# JavaScript 日期设置毫秒()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-set 毫秒-method/](https://www.geeksforgeeks.org/javascript-date-setmilliseconds-method/)

下面是**Date setmillies()**方法的例子。

*   **例:**

    ```
    <script>
       // Here a date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32:77');

       // New millisecond of 52 is being set in above Date
       // Object with the help of setMilliseconds() method
       dateobj.setMilliseconds(52);

       // New millisecond from above Date Object is
       // being extracted using getMilliseconds()
       var B = dateobj.getMilliseconds();

       // Printing new millisecond
       document.write(B);
    </script>
    ```

*   **输出:**

    ```
    52
    ```

**date . SetMixels()**方法用于在使用 date()构造函数创建的日期对象中设置毫秒。

**语法:**

```
dateObj.setMilliseconds(milliseconds_Value);
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **milliseconds_Value:** This parameter holds the value of millisecond which is used to set in date() constructor.

    **返回值:**返回新的，即更新的毫秒数，该毫秒数是由 set 毫秒()方法设置的。

    **注意:****DateObj**是使用 Date()构造函数创建的有效日期对象，我们希望在该构造函数中设置毫秒。毫秒的值从 0 到 999。

    上述方法的更多代码如下:

    **程序 1:** 如果在 Date()构造函数中我们没有给出任何毫秒，仍然 setMilliseconds()方法设置新的毫秒，该毫秒作为其参数给出。

    ```
    <script>
       // Here millisecond has not been assigned
       // while creating Date object
       var dateobj = new Date('October 13, 1996');

       // New millisecond of 51 is being set in above Date
       // Object with the help of setMilliseconds() method
       dateobj.setMilliseconds(51);

       // New millisecond from above Date Object is
       // being extracted using getMilliseconds()
       var B = dateobj.getMilliseconds();

       // Printing new millisecond
       document.write(B);
    </script>
    ```

    **输出:**

    ```
    51
    ```

    **程序 2:** 如果 Date()构造函数中没有给定任何参数，setMilliseconds()方法仍然设置毫秒，但是月、年、日期等变成当前的。这里 42 是新的毫秒，4 是当前月份，即 4 月，1 是当前日期，2018 是当前年份。

    ```
    <script>
       // Here nothing has been assigned
       // while creating Date object
       var dateobj = new Date();

       // new millisecond of 42 is being set in 
       // above Date Object with the help of 
       // setMilliseconds() method
       dateobj.setMilliseconds(42);

       // Milliseconds from above Date Object is
       // being extracted using getMilliseconds()
       var B = dateobj.getMilliseconds();

       // Month from above Date Object is
       // being extracted using getMonth()
       var C = dateobj.getMonth();

       // Date from above Date Object is
       // being extracted using getDate()
       var D = dateobj.getDate();

       // Year from above Date Object is
       // being extracted using getFullYear()
       var E = dateobj.getFullYear();

       // Printing new milliseconds
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
    4
    1
    2018
    ```

    **例 3:** 如果给定毫秒 1006 的值作为 setMixels()方法的参数，它将设置 6 为毫秒，因为毫秒范围是从 0 到 999，因此![1006-1000=6](img/74c480d28fb7d59c382d28f05479081b.png "Rendered by QuickLaTeX.com")，这里减去 1000 是因为 0 到 999 是 1000。
    这里 6 是新的毫秒，秒从 32 变成 33，因为毫秒范围是从 0 到 999，即总计 1000，我们将新的毫秒设置为 1006，它从 32 增加 1 秒到 33，毫秒变成 6。

    ```
    <script>
       // Here date has been assigned
       // while creating Date object
       var dateobj = 
       new Date('October 13, 1996 05:35:32:45');

       // new millisecond of 1006 is being set 
       // in above Date Object with the help of 
       // setMilliseconds() method
       dateobj.setMilliseconds(1006);

       // milliseconds from above Date Object is
       // being extracted using getMilliseconds()
       var B = dateobj.getMilliseconds();

       // Second from above Date Object is
       // being extracted using getSeconds()
       var C = dateobj.getSeconds();

       // Printing new Milliseconds
       document.write(B + "<br />");

       // Printing second
       document.write(C);
    </script>
    ```

    **输出:**

    ```
    6
    33
    ```

    **支持的浏览器:****JavaScript Date setmillies()方法**支持的浏览器如下:

    *   谷歌 Chrome 1 及以上版本
    *   边缘 12 及以上
    *   Firefox 1 及以上版本
    *   Internet Explorer 4 及以上版本
    *   歌剧 4 及以上
    *   Safari 1 及以上