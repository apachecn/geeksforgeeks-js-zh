# 如何用 javascript 计算两个日期之间的天数？

> 原文:[https://www . geesforgeks . org/如何计算 javascript 中两个日期之间的天数/](https://www.geeksforgeeks.org/how-to-calculate-the-number-of-days-between-two-dates-in-javascript/)

在 JavaScript 中计算两个日期之间的天数，这是使用 date 对象进行任何计算所必需的。为此，首先，使用内置的 JavaScript **getTime()函数**获取日期的内部毫秒值。一旦两个日期都转换了，就从前面的日期中减去后面的日期，然后返回以毫秒为单位的差值。稍后，可以通过将两个日期的差值(以毫秒为单位)除以一天中的毫秒数来计算最终结果。
**语法:**

```
Date.getTime()
```

**进场 1:**

*   使用**新日期()**定义两个日期。
*   使用**date 2 . gettime()–date 1 . gettime()计算两个日期的时间差；**
*   计算两个日期之间的天数，将两个日期的时间差除以一天中的毫秒数 **(1000*60*60*24)**
*   使用**文档打印最终结果。write()** 。

**示例 1:** 以下 JavaScript 程序将说明解决方案

## java 描述语言

```
<script type = "text/javascript" >
    // JavaScript program to illustrate 
    // calculation of no. of days between two date 

    // To set two dates to two variables
    var date1 = new Date("06/30/2019");
var date2 = new Date("07/30/2019");

// To calculate the time difference of two dates
var Difference_In_Time = date2.getTime() - date1.getTime();

// To calculate the no. of days between two dates
var Difference_In_Days = Difference_In_Time / (1000 * 3600 * 24);

//To display the final no. of days (result)
document.write("Total number of days between dates  <br>"
               + date1 + "<br> and <br>" 
               + date2 + " is: <br> " 
               + Difference_In_Days);

</script>
```

**输出:**

```
Total number of days between dates 
Sun Jun 30 2019 00:00:00 GMT-0700 (Pacific Daylight Time)
and 
Tue Jul 30 2019 00:00:00 GMT-0700 (Pacific Daylight Time) is: 
30
```

**进场 2:**

*   通过使用新的**日期()**来定义当前日期，新的**日期将通过**日期给出当前日期和圣诞节日期。****
*   if 条件，以便在圣诞节已经过去的情况下计算总天数(这将计算当前日期和下一年圣诞节之间的天数)。
*   使用**math . round(Christmas()–present _ date . gettime())**除以一天的毫秒数，以毫秒为单位计算结果，然后转换为天数

**例 2:** 本例我们计算了圣诞节前的天数。

## java 描述语言

```
<script type = "text/javascript" >

    // One day Time in ms (milliseconds)
    var one_day = 1000 * 60 * 60 * 24

// To set present_dates to two variables
var present_date = new Date();

// 0-11 is Month in JavaScript
var christmas_day = new Date(present_date.getFullYear(), 11, 25)

// To Calculate next year's Christmas if passed already.
if (present_date.getMonth() == 11 && present_date.getdate() > 25)
    christmas_day.setFullYear(christmas_day.getFullYear() + 1)

// To Calculate the result in milliseconds and then converting into days
var Result = Math.round(christmas_day.getTime() - present_date.getTime()) / (one_day);

// To remove the decimals from the (Result) resulting days value
var Final_Result = Result.toFixed(0);

//To display the final_result value
document.write("Number of days remaining till christmas <br>" 
               + present_date + "<br> and <br>" 
               + christmas_day + " is: <br> " 
               + Final_Result);

</script>
```

**输出:**

```
Number of days remaining till christmas 
Sun Jun 30 2019 11:33:51 GMT-0700 (Pacific Daylight Time)
and 
Wed Dec 25 2019 00:00:00 GMT-0800 (Pacific Standard Time) is: 
178
```

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。