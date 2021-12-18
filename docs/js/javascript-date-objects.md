# JavaScript |日期对象

> 原文:[https://www.geeksforgeeks.org/javascript-date-objects/](https://www.geeksforgeeks.org/javascript-date-objects/)

**日期对象**是 JavaScript 语言的一种内置数据类型。用来和*日期*和*时间*一起工作。使用*新建*关键字创建日期对象，即 ***新建日期()*** 。日期对象可以使用 1970 年 1 月 1 日前后 1 亿天内**毫秒**精度的日期和时间。但是使用另一种方法，我们只能使用本地或世界协调时或格林尼治时间来获取和设置年、月、日、小时、分钟、秒和毫秒字段。所以我们可以用 date 对象来表示 275755 年之前的日期和时间。
有四种不同的方式来声明日期，基本的事情是日期对象是由**新的 Date()** 操作符创建的。
**语法:**

```
new Date()
new Date(milliseconds)
new Date(dataString)
new Date(year, month, date, hour, minute, second, millisecond)

```

**示例:**

*   **new Date():**
    **Parameters:** The **Date()** constructor creates a Date object which sets the current date and time depend on the browser’s time zone. It does not accepts any value.
    **Example:**

    ```
    <script> 
    // "geeks" is Date object
    var geeks = new Date(); 

    document.write(geeks);
    // Prints todays date 
    </script>    
    ```

    **输出:**我会返回当前的日月日年标准时间。

    ```
    Wed Jul 03 2019 19:01:35 GMT+0530 (India Standard Time)

    ```

*   **new Date(milliseconds):**
    **Parameters:** This method accepts single parameter **milliseconds** which indicates any **numeric** value. This argument is taken as the internal numeric representation of the date in milliseconds.
    **Example:**

    ```
    <script> 
    // "geeks" is Date object
    var geeks = new Date(4500); 

    document.write("Todays date : " + geeks);
    </script>    
    ```

    **输出:**

    ```
    Todays date : Thu Jan 01 1970 05:30:04 GMT+0530 (India Standard Time)

    ```

*   **new Date(datastring):**
    **Parameters:** This method accepts single parameter **dataString** which indicates any **string** value. It is a string representation of a date and return the datastring with the day.
    **Example:**

    ```
    <script> 
    // "geeks" is Date object
    var geeks = new Date("October 13, 2013 11:13:00"); 

    document.write("Datastring with day : " + geeks);
    </script>    
    ```

    **输出:**

    ```
    Datastring with day : Sun Oct 13 2013 11:13:00 GMT+0530 (India Standard Time)

    ```

    l

*   **new Date(year, month, date, hour, minute, second, millisecond):**
    **Parameters:** This method accepts seven parameters as mentioned above and described below:
    *   **年:** *代表年的整数*值。这应始终指定完整的年份，即使用 2018 年，而不是使用 18 年。
    *   **月:** *整数*代表月份的值。整数值是从 1 月的 0 开始到 12 月的 11。
    *   **日期:** *代表日期的整数*值。
    *   **小时:** *整数*值，表示 24 小时制中的小时。
    *   **分钟:** *代表分钟的整数*值。
    *   **秒:** *整数*代表秒的值。
    *   **毫秒:** *整数*代表毫秒的值。

    **示例:**

    ```
    <script> 
    // "geeks" is Date object
    var geeks = new Date(2014, 10, 24, 10, 33, 30, 0); 

    document.write(geeks);
    </script>                    
    ```

    **输出:**

    ```
    Mon Nov 24 2014 10:33:30 GMT+0530 (India Standard Time)

    ```

    **日期对象的属性:**

    *   **Prototype:** Prototype 允许我们给一个对象添加属性和方法。
    *   **日期构造器:**它定义了创建日期对象原型的函数。

    **Date 对象的一些方法:**这里有一些定义 Date 对象用法的方法，这些都是非静态的方法。

    **以下方法是根据当地时间返回所有值:**

    | 方法 | 描述 |
    | **[日期()](https://www.geeksforgeeks.org/javascript-date-now/)** | 它返回当天的日期和时间。 |
    | **[【get data()](https://www.geeksforgeeks.org/javascript-date-getdate-function/)** | 它返回指定日期的日期。 |
    | **[【get ay()](https://www.geeksforgeeks.org/javascript-date-getday-method/)** | 它返回指定日期的星期几。 |
    | **[年满()](https://www.geeksforgeeks.org/javascript-date-getfullyear-function/)T3** | 它返回指定日期的年份。 |
    | **年数()** | 此方法返回指定日期的年份。 |
    | **[【get hours()](https://www.geeksforgeeks.org/javascript-date-gethours-function/)** | 它返回指定日期的小时。 |
    | **[【get seconds()](https://www.geeksforgeeks.org/javascript-date-getmilliseconds-function/)** | 它返回指定日期的毫秒数。 |
    | **[【get inuts()](https://www.geeksforgeeks.org/javascript-date-getminutes-method/)** | 它返回指定日期的分钟数。 |
    | **[【get onth()](https://www.geeksforgeeks.org/javascript-date-getmonth-method/)** | 它返回指定日期中的月份。这也找月了。 |
    | **[【get econds()](https://www.geeksforgeeks.org/javascript-date-getseconds-method/)** | 此方法返回指定日期的秒数。 |
    | **[gettime()](https://www.geeksforgeeks.org/javascript-gettime-method/)T3** | 此方法以毫秒为单位以数值形式返回日期。 |
    | **[【setdate()](https://www.geeksforgeeks.org/javascript-date-setdate-function/)** | 此方法为指定日期设置一个月中的某一天。 |
    | **[setFullYear()](https://www.geeksforgeeks.org/javascript-date-setfullyear-function/)** | 此方法为指定日期设置整年。 |

    还有很多方法:

    **以下方法是根据世界时返回所有值:**

    | 方法 | 描述 |
    | [获取 TCDate()](https://www.geeksforgeeks.org/javascript-date-getutcdate-function/) | 它返回指定日期的月份。 |
    | **[【get tcday()](https://www.geeksforgeeks.org/javascript-date-getutcday-function/)** | 它返回指定日期的星期几。 |
    | **[财政年度()](https://www.geeksforgeeks.org/javascript-date-getutcfullyear-function/)** | 此方法返回指定日期的年份。 |
    | **[【get tchours()](https://www.geeksforgeeks.org/javascript-date-getutchours-function/)** | 它返回指定日期的小时数。 |
    | [获取 TCMilliseconds()](https://www.geeksforgeeks.org/javascript-date-getutcmilliseconds-function/) | 此方法返回指定日期的毫秒形式。 |
    | 获取 TCMinutes() | 此方法返回指定日期的分钟数。 |
    | [获取 TCMonth()](https://www.geeksforgeeks.org/javascript-date-getutcmonth-function/) | 此方法返回指定日期的月份。 |