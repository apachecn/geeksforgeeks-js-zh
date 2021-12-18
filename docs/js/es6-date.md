# 是 6 |日期

> 哎哎哎:# t0]https://www . geeksforgeeks . org/es 6-date/

**ES6 日期**定义为自世界协调时 1970 年 1 月 1 日午夜以来经过的毫秒数。日期对象可以由**新日期()**构造器创建。在 JavaScript 中，日期和时间都由 date 对象表示。

**施工人员:**

1.  **[日期()](https://www.geeksforgeeks.org/javascript-date-objects/)**–为当前时间和日期创建日期对象。

    ```
    var date = new Date();
    console.log(date);

    ```

2.  **[日期(毫秒)](https://www.geeksforgeeks.org/javascript-date-objects/)**–创建一个日期对象，其时间等于从世界协调时 1970 年 1 月 1 日起经过的毫秒数。

```
var date = new Date(1570991017113);
console.log(date);

```

*   **[【日期字符串】](https://www.geeksforgeeks.org/javascript-date-objects/)**–用指定的日期字符串创建一个日期对象，然后像[那样自动解析。

    ```
    var date = new Date("2019-10-11");
    console.log(date);

    ```](https://www.geeksforgeeks.org/javascript-date-parse/) *   **Date(year, monthIndex [, day [, hours [, minutes [, seconds [, milliseconds]]]]])** – Create a date object with the specified date in local time zone. The first two arguments are necessary and the rest are optional.

    ```
    var date = new Date(2019, 0, 11, 15, 45, 55, 55);
    console.log(date);

    ```

    **属性:**

    1.  **[Date.prototype:](https://www.geeksforgeeks.org/javascript-date-prototype-property/)** 它代表了 **Date** 构造器的原型。**日期原型**本身是一个普通的物体，而不是**日期**实例。它允许向日期对象添加属性。
    2.  **[Date . constructor:](https://www.geeksforgeeks.org/javascript-date-constructor-property/)**它返回创建 Date 对象实例的数组函数的引用。

    **方法:**

    1.  **[Date.now()](https://www.geeksforgeeks.org/javascript-date-now/) :** 返回世界协调时 1970 年 1 月 1 日 00:00:00 后经过的毫秒数。

        ```
        console.log(Date.now()); // 1571060400486 
        // i.e. number of milliseconds elapsed since January 1, 1970 00:00:00 UTC

        ```

    2.  **[Date.parse()](https://www.geeksforgeeks.org/javascript-date-parse/) :** 对于所提供的日期字符串表示形式，它返回自 1970 年 1 月 1 日 00:00:00 UTC 以来经过的毫秒数。

        ```
        console.log(Date.parse("2019-10-11")); // 1570800633000

        ```

    3.  **[日期。UTC()](https://www.geeksforgeeks.org/date-utc-javascript/) :** 它返回提供的日期自 1970 年 1 月 1 日 00:00:00 UTC 起经过的毫秒数，用逗号分隔。

        ```
        console.log(Date.parse("2019, 9, 11")); // 1570800633000

        ```

    **日期.原型方法:**

    1.  **[getDate():](https://www.geeksforgeeks.org/javascript-date-getdate-function/)** 它从给定的日期对象返回当月的日期。

        ```
        var d = new Date("2019-10-11");
        console.log(d.getDate()); // 11

        ```

    2.  **[getDay():](https://www.geeksforgeeks.org/javascript-date-getday-method/)** 它根据给定日期对象的本地时间返回 0 到 6 的星期几。

        ```
        var d = new Date("2019-10-11");
        console.log(d.getDay()); // 5 i.e Friday

        ```

    3.  **[getFullYear():](https://www.geeksforgeeks.org/javascript-date-getfullyear-function/)** 它返回给定日期对象的完整年份。

        ```
        var d = new Date("2019-10-11");
        console.log(d.getFullYear()); // 2019

        ```

    4.  **[getHours():](https://www.geeksforgeeks.org/javascript-date-gethours-function/)** 它返回给定日期对象的小时(0-23)。

        ```
        var d = new Date("2019-10-11 16:30:33");
        console.log(d.getHours()); // 16

        ```

    5.  **[get 毫秒():](https://www.geeksforgeeks.org/javascript-date-getmilliseconds-function/)** 它根据当地时间返回给定日期对象的毫秒数(0-999)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getMilliseconds()); // 0

        ```

    6.  **[getMinutes():](https://www.geeksforgeeks.org/javascript-date-getminutes-method/)** 它根据当地时间返回给定日期对象的分钟(0-59)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getMinutes()); // 30

        ```

    7.  **[getMonth():](https://www.geeksforgeeks.org/javascript-date-getmonth-method/)** 根据当地时间返回给定日期对象的月份(0-11)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getMonth()); // 9

        ```

    8.  **[getSeconds():](https://www.geeksforgeeks.org/javascript-date-getseconds-method/)** 根据当地时间返回给定日期对象的秒(0-59)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getSeconds()); // 33

        ```

    9.  **[getTime():](https://www.geeksforgeeks.org/javascript-gettime-method/)** 它返回自 1970 年 1 月 1 日 00:00:00 UTC 以来经过的毫秒数。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getTime()); // 1570791633000

        ```

    10.  **[getTimezoneOffset():](https://www.geeksforgeeks.org/javascript-date-gettimezoneoffset-with-examples/)**它以分钟为单位返回 UTC 和本地时区之间的差值。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getTimezoneOffset()); // -330

        ```

    11.  **[getutctdate():](https://www.geeksforgeeks.org/javascript-date-getutcdate-function/)**它根据给定日期对象的世界时返回一个月中的某一天(1-31)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCDate()); // 11

        ```

    12.  **[getUTCDay():](https://www.geeksforgeeks.org/javascript-date-getutcday-function/)** 它根据给定日期对象的世界时返回一周中的某一天(0-6)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCDay()); // 5

        ```

    13.  **[getutfullyear():](https://www.geeksforgeeks.org/javascript-date-getutcfullyear-function/)**它根据给定日期对象的世界时返回年份。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCFullYear()); // 2019

        ```

    14.  **[getutchows():](https://www.geeksforgeeks.org/javascript-date-getutchours-function/)**根据给定日期对象的世界时返回小时(0-23)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCHours()); // 11

        ```

    15.  **[getutcmails():](https://www.geeksforgeeks.org/javascript-date-getutcmilliseconds-function/)**它根据给定日期对象的世界时返回毫秒(0-999)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCMilliseconds()); // 0

        ```

    16.  **[getutchminutes():](https://www.geeksforgeeks.org/javascript-date-getutcminutes-function/)**它根据给定日期对象的世界时返回分钟。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCMinutes()); // 0

        ```

    17.  **[getutchmonth():](https://www.geeksforgeeks.org/javascript-date-getutcmonth-function/)**根据给定日期对象的世界时返回月份(0-11)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCMonth()); // 9

        ```

    18.  **[getutcsters():](https://www.geeksforgeeks.org/javascript-date-getutcseconds-function/)**根据给定日期对象的世界时返回秒(0-59)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        console.log(d.getUTCSeconds()); // 33

        ```

    19.  **[setDate():](https://www.geeksforgeeks.org/javascript-date-setdate-function/)** 用于将一个月的日期设置为当地时间的日期对象。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setDate(13);
        console.log(d.getDate()); // 13

        ```

    20.  **[setFullYear():](https://www.geeksforgeeks.org/javascript-date-setfullyear-function/)** 用于将年设置为当地时间的日期对象。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setYear(2018);
        console.log(d.getFullYear()); // 2018

        ```

    21.  **[setHours():](https://www.geeksforgeeks.org/javascript-date-sethours-function/)** 用于设置本地时间中日期对象的小时(0-23)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setHours(19);
        console.log(d.getHours()); // 19

        ```

    22.  **[setmillises():](https://www.geeksforgeeks.org/javascript-date-setmilliseconds-function/)**用于设置本地时间中日期对象的毫秒数。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setMilliseconds(200);
        console.log(d.getMilliseconds()); // 200

        ```

    23.  **[setMinutes():](https://www.geeksforgeeks.org/javascript-date-setminutes-function/)** 用于设置当地时间中日期对象的分钟数(0-59)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setMinutes(20);
        console.log(d.getMinutes()); // 20

        ```

    24.  **[setMonth():](https://www.geeksforgeeks.org/javascript-date-setmonth-function/)** 用于将月份(0-11)设置为当地时间的日期对象。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setMonth(8);
        console.log(d.getMonth()); // 8

        ```

    25.  **[setSeconds():](https://www.geeksforgeeks.org/javascript-date-setseconds-function/)** 用于设置当地时间的日期对象的秒数(0-59)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setSeconds(34);
        console.log(d.getSeconds()); // 34

        ```

    26.  **[setTime():](https://www.geeksforgeeks.org/date-settime-method-in-java-with-examples/)** 用于将世界协调时 1970 年 1 月 1 日 00:00:00 后的毫秒设置为本地时间中的日期对象。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setTime(1570815753000);
        console.log(d.toDateString()); // "Fri Oct 11 2019"

        ```

    27.  **[setutctdate():](https://www.geeksforgeeks.org/javascript-date-setutcdate-function/)**用于根据世界时为日期对象设置月份的日期(0-11)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setUTCDate(12);
        console.log(d.getDate()); // 12

        ```

    28.  **[setutfullyear():](https://www.geeksforgeeks.org/javascript-date-setutcfullyear-function/)**用于根据世界时将年设置为日期对象。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setUTCFullYear(2018);
        console.log(d.getFullYear()); // 2018

        ```

    29.  **[setutchows():](https://www.geeksforgeeks.org/javascript-date-setutchours-function/)**用于根据世界时给日期对象设置小时(0-23)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setUTCHours(16);
        console.log(d.getHours()); // 21

        ```

    30.  **[setutcmails():](https://www.geeksforgeeks.org/javascript-date-setutcmilliseconds-function/)**用于根据世界时给日期对象设置毫秒。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setUTCMilliseconds(166);
        console.log(d.getMilliseconds()); // 166

        ```

    31.  **[setutcments():](https://www.geeksforgeeks.org/javascript-date-setutcminutes-function/)**用于根据世界时给日期对象设置分钟(0-59)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setUTCMinutes(22);
        console.log(d.getMinutes()); // 52

        ```

    32.  **[setutchmonth():](https://www.geeksforgeeks.org/javascript-date-setutcmonth/)**用于根据世界时给日期对象设置月份(0-11)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setUTCMonth(8);
        console.log(d.getMonth()); // 8

        ```

    33.  **[setutctseconds():](https://www.geeksforgeeks.org/javascript-date-setutcseconds-function/)**用于根据世界时给日期对象设置秒(0-59)。

        ```
        var d = new Date("October 11, 2019 16:30:33");
        d.setUTCSeconds(10);
        console.log(d.getSeconds()); // 10

        ```

    **日期转换方法:**

    1.  **[todaytestring():](https://www.geeksforgeeks.org/javascript-date-todatestring-function/)**它返回日期对象的日期部分的字符串表示形式。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toDateString()); // "Fri Oct 11 2019"

        ```

    2.  **[toISOString():](https://www.geeksforgeeks.org/javascript-date-todatestring-function/)** 它使用 ISO 8601 扩展格式返回日期对象的日期部分的字符串表示形式。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toISOString()); // "2019-10-11T14:00:33.000Z"

        ```

    3.  **[toJSON():](https://www.geeksforgeeks.org/javascript-date-tojson-function/)** 它返回日期对象的日期部分的字符串表示。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toJSON()); // "2019-10-11T14:00:33.000Z"

        ```

    4.  **[to localeDateString():](https://www.geeksforgeeks.org/javascript-date-tolocaledatestring/)**它接受两个参数(可选)–**区域设置**和**选项**，并根据指定的区域设置返回日期部分的字符串表示。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toLocaleDateString()); // "10/11/2019"

        // 10.2019
        console.log(d.toLocaleDateString("de-DE", {year:'numeric', month: 'numeric'}))

        ```

    5.  **[to localestring():](https://www.geeksforgeeks.org/javascript-date-tolocalestring/)**它以区域设置格式返回日期部分的日期对象字符串。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toLocaleString()); // "10/11/2019, 7:30:33 PM"

        ```

    6.  **[tolocalitemestring():](https://www.geeksforgeeks.org/javascript-date-tolocaletimestring/)**它返回日期对象的时间部分的字符串表示形式。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toLocaleTimeString()); // "7:30:33 PM"

        ```

    7.  **[toString():](https://www.geeksforgeeks.org/javascript-date-tostring-function/)** 它返回日期对象的日期的字符串表示形式。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);

        // "Fri Oct 11 2019 19:30:33 GMT+0530 (India Standard Time)"
        console.log(d.toString()); 

        ```

    8.  **[toTimeString():](https://www.geeksforgeeks.org/javascript-date-totimestring-function/)** 它返回日期对象的时间部分的字符串表示。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toTimeString()); // "19:30:33 GMT+0530 (India Standard Time)"

        ```

    9.  **[【TouchString():](https://www.geeksforgeeks.org/javascript-date-toutcstring-function/)**它以通用时区的格式返回日期对象的字符串表示形式。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.toUTCString()); // "Fri, 11 Oct 2019 14:00:33 GMT"

        ```

    10.  **[valueOf():](https://www.geeksforgeeks.org/javascript-date-valueof-function/)** 它返回从世界协调时 1970 年 1 月 1 日 00:00:00 到提供的日期之间经过的毫秒数。

        ```
        var d = new Date(2019, 9, 11, 19, 30, 33);
        console.log(d.valueOf()); // 1570802433000

        ```