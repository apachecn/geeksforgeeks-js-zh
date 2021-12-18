# JavaScript Date to localetimestring()方法

> 原文:[https://www . geesforgeks . org/JavaScript-date-tolocalitemestring-method/](https://www.geeksforgeeks.org/javascript-date-tolocaletimestring-method/)

下面是 **Date toLocaleTimeString()** 方法的例子。

*   **例:**

    ```
    <script>
      // Here a date has been assigned
      // while creating Date object
      var dateobj = new Date('July 16, 2018 05:35:32');

      // time from above date object is 
      // being extracted using toLocaleTimeString()
      var B = dateobj.toLocaleTimeString();

      // Printing time
      document.write(B);

    </script>
    ```

*   **输出:**

    ```
    5:35:32 
    ```

方法用于从给定的日期对象中获取时间。
**语法:**

```
DateObj.toLocaleTimeString()
```

**参数:**此方法不接受任何参数。它只是与我们想要从中获取时间的日期对象一起使用。

**返回值:**返回给定日期对象的时间字符串。

**注意:****DateObj**是一个使用 Date()构造函数创建的有效日期对象，我们希望从中获取时间。

上述方法的更多代码如下:

**程序 1:** 月份的日期应该在 1 到 31 之间，因为没有一个月份的日期大于 31，这就是为什么它返回无效日期，因为月份的日期不存在。因此，当月份日期为 36，即大于 31 时，年就不存在了。

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = new Date('July 36, 2018 05:35:32');

  // time from above date object is
  // being extracted using toLocaleTimeString()
  var B = dateobj.toLocaleTimeString();

  // Printing time
  document.write(B);  

</script>
```

**输出:**

```
Invalid Date
```

**程序 2:** 如果没有给 date()构造函数任何参数，那么当前日期将被传递到 Date 对象中，因此 toLocaleTimeString()将返回当前时间。

```
<script>
  // Here a date has been assigned
  // while creating Date object
  var dateobj = new Date();

  // time from above date object is
  // being extracted using toLocaleTimeString()
  var B = dateobj.toLocaleTimeString();

  // Printing time
  document.write(B);     
</script>
```

**输出:**本程序返回的时间为**当前时间**

```
4:09:16 

```

**支持的浏览器:**JavaScript Date to localetimestring()方法支持的浏览器如下:

*   谷歌 Chrome 及以上
*   边缘 12 及以上
*   Firefox 1 及以上版本
*   Internet Explorer 5.5 及以上版本
*   歌剧 5 及以上
*   Safari 1 及以上