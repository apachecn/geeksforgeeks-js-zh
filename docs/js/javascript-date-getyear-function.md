# JavaScript | date.getYear()函数

> 原文:[https://www . geesforgeks . org/JavaScript-date-getyear-function/](https://www.geeksforgeeks.org/javascript-date-getyear-function/)

JavaScript 中的 **date.getYear()** 方法是根据世界时得到指定日期的*年*。我们从 getYear()方法得到的年份是当前年份减去 1900。

**语法:**

```
date.getYear()
```

这里，日期是 **Date()** 类的对象。

**参数:**此功能不接受任何参数。
**返回值:**此方法返回一个从 1900 年减去当前年份的值。

**例 1:** 本例根据世界时返回指定日期的年份。

## java 描述语言

```
<script>

// "date" is object of Date() class
var date = new Date();

// Use "getYear()" method and stores
// the returned value to "n"
var n = date.getYear();

// Display the result
document.write("The value returned by getYear() method: " + n)

</script>                   
```

**输出:**

```
The value returned by getYear() method: 119
```

**例 2:** 本例只向构造函数发送年份。

## java 描述语言

```
<script>

// Year 2000 is assign to the
// constructor of Date() class
var date = new Date('2000')

// Use "getYear()" method and stores
// the returned value to "n"
var n = date.getYear();

// Display the returned value
// The value is the subtraction of
// 2000 and 1900  
document.write("The value returned by getYear() method: " + n)

</script>
```

**输出:**

```
The value returned by getYear() method: 100
```

**例 3:** 这里我们给构造函数传递一个完整的日期，日期的格式为*月-日-年-时*，如**2010 年 10 月 15 日 02:05:32** 。

## java 描述语言

```
<script>

// Full date is assign to the constructor of Date() class
var date = new Date('October 15, 2010, 02:05:32')

// Use "getYear()" method and stores the
// returned value in "n"    
var n = date.getYear();

// Display the returned value
// The value is the subtraction of 2010 and 1900  
document.write("The value returned by getYear() method: " + n)

</script>
```

**输出:**

```
The value returned by getYear() method: 110
```