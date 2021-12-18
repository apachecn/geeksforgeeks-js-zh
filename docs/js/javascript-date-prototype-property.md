# JavaScript 日期原型属性

> 原文:[https://www . geesforgeks . org/JavaScript-date-prototype-property/](https://www.geeksforgeeks.org/javascript-date-prototype-property/)

下面是**日期原型属性**的例子。

*   **例:**

    ```
    <script>

      var birthday = new Date('June 21, 2018 16:44:23');
      var date1 = birthday.getDate(); 
      var day1 = birthday.getDay(); 
      var year1 = birthday.getFullYear(); 
      var hour1 = birthday.getHours(); 
      var ms1 = birthday.getMilliseconds(); 
      var m1 = birthday.getMinutes(); 
      var mth1 = birthday.getMonth(); 
      var time1 = birthday.getTime(); 
      var s1 = birthday.getSeconds(); 
      var offset = birthday.getTimezoneOffset(); 
      var date2 = birthday.getUTCDate(); 
      var day2 = birthday.getUTCDay(); 
      var year2 = birthday.getUTCFullYear(); 
      var hour2 = birthday.getUTCHours(); 
      var ms2 = birthday.getUTCMilliseconds();
      var um1 = birthday.getUTCMinutes();
      var umth = birthday.getUTCMonth();
      var us = birthday.getUTCSeconds();

      document.write(date1 +"<br>");
      document.write(day1 +"<br>");
      document.write(year1 +"<br>");
      document.write(hour1 +"<br>");
      document.write(ms1 +"<br>");
      document.write(m1 +"<br>");
      document.write(mth1 +"<br>");
      document.write(time1 +"<br>");
      document.write(s1 +"<br>");
      document.write(offset +"<br>");
      document.write(date2 +"<br>");
      document.write(day2 +"<br>");
      document.write(year2 +"<br>");
      document.write(hour2 +"<br>");
      document.write(ms2 +"<br>");
      document.write(um1 +"<br>");
      document.write(umth +"<br>");
      document.write(us);        
    </script>
    ```

*   **输出:**

    ```
    21
    4
    2018
    16
    0
    44
    5
    1529579663000
    23
    -330
    21
    4
    2018
    11
    0
    14
    5
    23

    ```

**注意:****Date . prototype**属性代表日期构造函数的原型。

**有以下方法:**

*   **[getDate()](https://www.geeksforgeeks.org/javascript-date-getdate-method/) :**
    此方法会根据当地时间返回指定日期的月份中的某一天。
*   **[getDay()](https://www.geeksforgeeks.org/javascript-date-getday-method/) :**
    此方法将根据当地时间返回指定日期的一周中的某一天(周日为 0，周六为 6)。
*   **[getFullYear()](https://www.geeksforgeeks.org/javascript-date-getfullyear-method/) :** 根据当地时间返回指定日期的年份。
*   **[getHours()](https://www.geeksforgeeks.org/javascript-date-gethours-method/) :** 根据当地时间返回指定日期的小时(0-23)。
*   **[get 毫秒:](https://www.geeksforgeeks.org/javascript-date-getmilliseconds-method/)** 根据当地时间返回指定日期的毫秒数(0-999)。
*   **[getMinutes()](https://www.geeksforgeeks.org/javascript-date-getminutes-method/) :** 根据当地时间返回指定日期的分钟数(0-59)。
*   **[getMonth()](https://www.geeksforgeeks.org/javascript-date-getmonth-method/) :** 根据当地时间返回指定日期的月份(0-11)。
*   **[getSeconds()](https://www.geeksforgeeks.org/javascript-date-getseconds-method/) :** 根据当地时间返回指定日期的秒(0-59)。
*   **[getTime():](https://www.geeksforgeeks.org/javascript-date-gettime-method/)** 它返回自 1970 年 1 月 01 日 00:00:00 UTC 以来埃勒馥的毫秒数。在给定时间之前
    时间为负。
*   **[gettimeozneofset()](https://www.geeksforgeeks.org/javascript-date-gettimezoneoffset-method/):**返回当前位置的时区偏移量，以分钟为单位。
*   **[getutctdate()](https://www.geeksforgeeks.org/javascript-date-getutcdate-method/):**根据世界时返回指定日期的月份日期(1-31)。
*   **[getUTCDay()](https://www.geeksforgeeks.org/javascript-date-getutcday-method/) :** 根据世界时返回指定日期的星期几(0-6)。
*   **[getUTCFullYear()](https://www.geeksforgeeks.org/javascript-date-getutcfullyear-method/):**根据世界时返回指定日期的年份。
*   **[getutchows()](https://www.geeksforgeeks.org/javascript-date-getutchours-method/):**根据世界时返回指定日期的小时(0-23)。
*   **[getutcmails()](https://www.geeksforgeeks.org/javascript-date-getutcmilliseconds-method/):**根据世界时返回指定日期的毫秒数(0-999)。
*   **[getutchminutes()](https://www.geeksforgeeks.org/javascript-date-getutcminutes-method/):**根据世界时返回指定日期的分钟数(0-59)。
*   **[getutchmonth()](https://www.geeksforgeeks.org/javascript-date-getutcmonth-method/):**根据世界时返回指定日期的月份(0-11)。
*   **[getutctseconds()](https://www.geeksforgeeks.org/javascript-date-getutcseconds-method/):**根据世界时返回指定日期的秒(0-59)。

**它还有一些其他的方法可以把日期转换成不同的格式:**

*   **[todaytestring()](https://www.geeksforgeeks.org/javascript-date-todatestring-function/):**以人类可读的字符串形式返回日期的“日期”部分。
*   **toGMTString():** 根据格林尼治标准时间(UT)时区返回表示日期的字符串。
*   **toLocaleFormat():** 使用格式字符串将日期转换为字符串。
*   **[ToLocalString()](https://www.geeksforgeeks.org/javascript-date-tolocalestring/):**返回一个字符串，该字符串具有该日期的位置敏感表示。
*   **[toString()](https://www.geeksforgeeks.org/javascript-tostring-function/) :** 返回表示指定日期对象的字符串。
*   **[toTimeString()](https://www.geeksforgeeks.org/javascript-date-totimestring-function/) :** 将日期的“时间”部分作为人类可读的字符串返回。
*   **[valueOf()](https://www.geeksforgeeks.org/javascript-date-valueof-function/) :** 返回日期对象的原始值。

**支持的浏览器:****JavaScript 日期原型属性**支持的浏览器如下:

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   Mozilla Firefox
*   歌剧
*   旅行队