# 如何在 JavaScript 中将 CFAbsoluteTime 转换为 Date 对象，反之亦然？

> 原文:[https://www . geesforgeks . org/how-convert-cfabsolutetime-to-date-object-反之亦然-in-javascript/](https://www.geeksforgeeks.org/how-to-convert-cfabsolutetime-to-date-object-and-vice-versa-in-javascript/)

CFAbsolute time 是苹果设备和 Swift 等编程语言上的标准时间格式。它存储自 2001 年 1 月 1 日以来的纳秒量。它的核心类似于纪元时间，只是它存储的时间更接近现代，使用 2001 年作为参考点，而不是 1970 年。这是苹果官方的绝对时间文档。

为了将 CFAbsoluteTime 转换为 Date 对象，反之亦然，我们将主要使用 JavaScript Date.getTime()方法，该方法提供了自 1970 年 1 月 1 日以来的毫秒数。我们还将使用 Date.setTime()方法，该方法设置自 1970 年 1 月 1 日以来的毫秒数。

#### 从绝对时间转换为日期对象

要从 CFAbsolute time 转换为正常日期，我们可以从 2001 年 1 月 1 日创建一个 date 对象，并简单地将 CFAbsolute Time 值(以毫秒为单位)添加到 Date.getTime()值中。

## Javascript

```
const CFAbsoluteTimeToDate = (CFATime,
    unitConversionValue = 1000) => {
    const dt = new Date('January 1 2001 GMT');
    dt.setTime(dt.getTime() + CFATime * unitConversionValue);
    return dt;
};

console.log(CFAbsoluteTimeToDate(639494700));
```