# 如何在 JavaScript 中获取纪元以来的秒数？

> 原文:[https://www . geeksforgeeks . org/如何获取 javascript 中的自纪元以来的秒数/](https://www.geeksforgeeks.org/how-to-get-seconds-since-epoch-in-javascript/)

给定一个日期，我们必须找到自纪元以来的秒数(即 1970 年 1 月 1 日，世界协调时 00:00:00)。JavaScript 中的 **[getTime()方法](https://www.geeksforgeeks.org/javascript-gettime-method/)** 返回自 1970 年 1 月 1 日以来的毫秒数，即纪元。如果我们将这些毫秒除以 1000，整数部分将给出自纪元以来的秒数。

**例:**

```
Input: Date = 27-04-2020, 11:55:55
Output: Seconds since epoch - 1587968755

```

**语法:**

```
new Date(year, month, day, hours, minutes, seconds, milliseconds)
```

**例:**

```
<script type="text/javascript">
    function seconds_since_epoch(d){ 
        return Math.floor( d / 1000 ); 
    }

    // Driver Code
    var d = new Date(2020, 4, 29, 22, 00, 00, 00);
    var sec = seconds_since_epoch(d);
    document.write("Date " + d + " has " 
                   + sec+ " seconds till epoch.");
</script>                    
```

**输出:**

```
Date Fri May 29 2020 22:00:00 GMT+0530 (India Standard Time) 
has 1590769800 seconds till epoch.
```