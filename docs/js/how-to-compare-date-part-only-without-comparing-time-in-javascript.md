# 如何在 JavaScript 中只比较日期部分而不比较时间？

> 原文:[https://www . geesforgeks . org/如何比较日期-仅部分-不比较时间-javascript/](https://www.geeksforgeeks.org/how-to-compare-date-part-only-without-comparing-time-in-javascript/)

为了在 javascript 中获取日期和时间，我们有 **Date()** 类。我们通过创建对象来访问**日期()**类。**日期()**类返回日期和时间的总和。

实例化日期有四种方式:
**语法:**

```
var d = new Date();
//returns the present date and time
```

或者

```
var d = new Date(milliseconds);
//to set a specific date
```

或者

```
var d = new Date(dateString);
//to set a specific date
```

或者

```
var d = new Date(year, month, day, hours, minutes, seconds, milliseconds);
//to set a specific date:
```

因此 Date()返回**函数 Date(){[本机代码] }** ，我们可以使用 **object.toString()** 将其转换为字符串

**方法 1:**
当物体被比较时，它会被与时间和日期进行比较。
现在我们将时间设置为 00:00:00(停止)，这样当对象被比较时，只有日期被比较，因为两个日期对象的时间都是 00:00:00(停止)。

要将时间设置为 00:00:00(停止)， **setHours()** 就派上用场了。

**语法；**

```
//the hour(0-23) is mandatory.
dateobject.setHours(hour, min, sec, millisec)

```

为了使时间为 0 或完全停止，我们必须确保所有参数为 0，包括毫秒。

**示例:**

```
<!DOCTYPE html>
<html>

<body>

    <p>Below date1 and data2 are compared for older, further, and same dates.</p>

    <script>
        //Example-1
        var date1 = new Date();
        date1.setHours(0, 0, 0, 0)
        var date2 = new Date(2020, 8, 20);
        //stops the clock
        date2.setHours(0, 0, 0, 0)
        document.write("date1=>", date1);
        document.write("<br \>date2=>", date2);
        if (date1 > date2) {
            document.write("<br \>date1 is further than date2");
        } else if (date1 < date2) {
            document.write("<br \>date1 is older than date2")
        } else {
            document.write("<br \>date1 and date2 same")
        }
        //Example-2
        date2 = new Date(2019, 11, 3);
        document.write("<br \><br \>date1=>", date1);
        document.write("<br \>date2=>", date2);
        if (date1 > date2) {
            document.write("<br \>date1 is further than date2");
        } else if (date1 < date2) {
            document.write("<br \>date1 is older than date2")
        } else {
            document.write("<br \>date1 and date2 same")
        }
        //Example-3
        date1 = new Date();
        date2 = new Date();
        date1.setHours(0, 0, 0, 0)
        date2.setHours(0, 0, 0, 0)
        document.write("<br \><br \>date1=>", date1);
        document.write("<br \>date2=>", date2);
        if (date1 > date2) {
            document.write("<br \>date1 is further than date2");
        } else if (date1 < date2) {
            document.write("<br \>date1 is older than date2")
        } else {
            document.write("<br \>date1 and date2 same.")
        }
        //Example-4
        date1 = new Date();
        date2 = new Date();
        date1.setHours(0, 0, 0, 0)
            /*Due to, time didn't get stop in data2,
            it’s time also gets compared to data1.*/
            //date2.setHours(0,0,0,0)
        document.write("<br \><br \>date1=>", date1);
        document.write("<br \>date2=>", date2);
        if (date1 > date2) {
            document.write("<br \>date1 is further than date2");
        } else if (date1 < date2) {
            document.write("<br \>date1 is older than date2")
        } else {
            document.write("<br \>date1 and date2 same.")
        }
    </script>

</body>

</html>
```

**输出**

```
Below date1 and data2 are compared for older, further, and same dates.

date1=>Wed Dec 04 2019 00:00:00 GMT+0530 (India Standard Time)
date2=>Sun Sep 20 2020 00:00:00 GMT+0530 (India Standard Time)
date1 is older than date2

date1=>Wed Dec 04 2019 00:00:00 GMT+0530 (India Standard Time)
date2=>Tue Dec 03 2019 00:00:00 GMT+0530 (India Standard Time)
date1 is further than date2

date1=>Wed Dec 04 2019 00:00:00 GMT+0530 (India Standard Time)
date2=>Wed Dec 04 2019 00:00:00 GMT+0530 (India Standard Time)
date1 and date2 same.

date1=>Wed Dec 04 2019 00:00:00 GMT+0530 (India Standard Time)
date2=>Wed Dec 04 2019 05:37:26 GMT+0530 (India Standard Time)
date1 is older than date2

```

**方法 2:**
这里我们将使用**todaytestring()**来获取唯一的日期，但是当获取时它被转换为字符串，因为字符串的比较是不可能的，我们需要获取然后再次转换为日期对象，现在当将它们转换回对象时时间设置为 *00:00:00(stops)* 。

**语法:**

```
var date1 = new Date(new Date().toDateString());
```

**上述语法的分解**

```
new Date().toDateString()
converts the Date object to a string containing only the date part.
```

```
new Date(new Date().toDateString()); 
converts it back to Date object setting time to 00:00:00

```

**例**

```
<!DOCTYPE html>
<html>

<body>

    <p>Below date1 and data2 are compared for older,
      further, and same dates.</p>

    <script>
        //Example-1
        var date1 = new Date(new Date().toDateString());
        var date2 = new Date(new Date(2018, 8, 20).toDateString());
        //var date2 = new Date(2018,8,20).toDateString();
        document.write("date1=>", date1); //returns only the date.
        document.write("<br \>date2=>", date2);
        if (date1 > date2) {
            document.write("<br \>date1 is further than date2");
        } else if (date1 < date2) {
            document.write("<br \>date1 is older than date2")
        } else {
            document.write("<br \>date1 and date2 same")
        }
    </script>
</body>

</html>
```

**输出**

```
Below date1 and data2 are compared for older, further, and same dates.

date1=>Fri Dec 20 2019 00:00:00 GMT+0530 (India Standard Time)
date2=>Thu Sep 20 2018 00:00:00 GMT+0530 (India Standard Time)
date1 is further than date2

```