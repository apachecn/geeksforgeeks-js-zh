# JavaScript Date to localestring()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-tolocalesting-method/](https://www.geeksforgeeks.org/javascript-date-tolocalestring-method/)

下面是 **Date toLocaleString()** 方法的例子。

*   **例:**

    ```
    <script>
        var d = new Date(Date.UTC(2020, 9, 26, 7, 0, 0));
        var result = d.toLocaleString();
        document.write("Date and Time of apocalypse: "
        + result);
    </script>                    
    ```

*   **Output:**

    ```
    Date and Time of apocalypse: 26/10/2020, 12:30:00
    ```

    方法用于将日期和时间转换为字符串。
    **语法:**

    ```
    dateObj.toLocaleString(locales, options)
    ```

    **参数:**该方法接受两个参数，如上所述，如下所述:

    *   **地区:**此参数是包含一个或多个语言或地区标记的地区字符串数组。请注意，它是一个可选参数。如果您想在应用程序中使用特定的语言格式，那么请在 locales 参数中指定该语言。
    *   **选项:**也是可选参数，包含指定比较选项的属性。有些属性是 localeMatcher、时区、工作日、年、月、日、小时、分钟、秒等。

    **返回值:**它以区域设置指定的特定格式将日期和时间作为字符串值返回。

    **注意:****日期对象**应该是有效的日期对象。

    **程序 1:** 该代码打印当前日期和时间。此外，在这段代码中 **toLocaleString()** 方法不使用任何参数，因此它使用操作系统的区域设置约定并返回特定于机器的结果。

    ```
    <script>
      var d = new Date();
      var result = d.toLocaleString();
      document.write("date and time as a string =  " + result);
    </script>

    ```

    **输出:**

    ```
    date and time as a string = 6/26/2018, 10:28:17 
    ```

    **程序 2:** 该代码以区域设置参数指定的字符串格式打印日期和时间。

    ```
    <script>
      var date = new Date(Date.UTC(2018, 5, 26, 7, 0, 0));  
      var options = { hour12: false };  
      document.write(date.toLocaleString("en-US"));
      document.write("<br>");
      document.write(date.toLocaleString("en-US", options));
    </script>
    ```

    **输出:**

    ```
    6/26/2018, 12:30:00 PM
    6/26/2018, 12:30:00

    ```

    **注意:****toLocaleString()**方法与**tolocaledatastring()**不同，因为**tolocaledatastring()**仅将 date 对象的日期转换为字符串，而 **toLocaleString()** 将日期和时间转换为字符串..

    **支持的浏览器:**JavaScript Date to localestring()方法支持的浏览器如下:

    *   谷歌 Chrome 1 及以上版本
    *   边缘 12 及以上
    *   Firefox 1 及以上版本
    *   Internet Explorer 3 及以上版本
    *   歌剧 3 及以上
    *   Safari 1 及以上