# 如何将 JavaScript 日期转换为 UTC？

> 原文:[https://www . geesforgeks . org/how-convert-a-JavaScript-date-utc/](https://www.geeksforgeeks.org/how-to-convert-a-javascript-date-to-utc/)

可以使用 Javascript date 对象中的函数将 Javascript 日期转换为 UTC。
根据世界时，使用**toutcsting()**方法将日期对象转换为字符串。
T4 时间字符串()返回一个基于格林尼治标准时间时区表示日期的字符串。

默认情况下，JavaScript 使用浏览器的时区并将日期显示为全文字符串: **Fri 2019 年 4 月 12 日 10:32:15 GMT+0530(印度标准时间)。**
要创建一个新的日期对象，我们使用 javascript **日期()**构造函数。

 **语法:**

```
dateObj.toUTCString()
```

**示例-1:**

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width, 
                   initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" 
          content="ie=edge">
    <title>
      Document
  </title>
</head>

<body>
    <div id="date">

    </div>
</body>
<script>
    var d = new Date();
    var n = d.toUTCString();
    var e = document.querySelector("#date");
    e.innerHTML = n;
</script>

</html>
```

**输出:**

```
Fri, 12 Apr 2019 05:14:31 GMT
```

**示例-2:**

```
<!DOCTYPE html>
<html lang="en">

<head>
    <meta charset="UTF-8">
    <meta name="viewport"
          content="width=device-width,
                   initial-scale=1.0">

    <meta http-equiv="X-UA-Compatible" 
          content="ie=edge">
    <title>
      Document
  </title>
</head>

<body>
    <div id="date">

    </div>
</body>
<script>
    var d = new Date();
    var e = document.querySelector("#date");
    e.innerHTML = d.toGMTString();
</script>

</html>
```

**输出:**

```
Fri, 12 Apr 2019 05:39:32 GMT
```

**引用**
[Javascript 日期对象](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Date)