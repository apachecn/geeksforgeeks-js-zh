# JavaScript 日期解析()方法

> 原文:[https://www.geeksforgeeks.org/javascript-date-parse-method/](https://www.geeksforgeeks.org/javascript-date-parse-method/)

下面是 **Date parse()** 方法的例子。

*   **例:**

## java 描述语言

```
<script>
    // Taking a date string as input.
    var date = "February 18, 2018 12:30 PM";

    // Calling parse function on input date string.
    var msec = Date.parse(date);
    document.write(msec);
</script>                   
```

*   **输出:**

```
1518937200000
```

**date.parse()** 方法用于知道从 1970 年 1 月 1 日午夜到我们提供的日期之间的确切毫秒数。
**语法:**

```
Date.parse(datestring);
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **日期字符串:**此参数将日期保存为字符串。

**返回值:**它返回一个整数值，表示 1970 年 1 月 1 日午夜和提供的日期之间的毫秒数。无论如何，如果机器无法识别字符串或输入字符串无效，它将返回“NaN”而不是整数。
以上方法的更多代码如下:
**程序 1:** 如果输入的日期字符串不正确，则返回 NaN，即不是数字。

## java 描述语言

```
<script>

    // Taking wrong date string as input.
    var date = "February 48, 2018 12:30 PM";

    // calling parse function.
    var msec = Date.parse(date);
    document.write(msec);

</script>                   
```

**输出:**

```
NaN
```

**程序 2:** 如果输入的日期字符串不正确，则返回 NaN，即不是数字。

## java 描述语言

```
<script>

    // Taking wrong date string as input.
    var date = "June 22, 2012";

    // Calling parse function.
    var msec = Date.parse(date);
    document.write(msec);

</script>                   
```

**输出:**

```
1340303400000
```

**注:**一旦得到两个日期之间的毫秒数，通过简单的数学计算就可以很容易地找到小时、天、月、年等的个数。
**支持的浏览器:**JavaScript Date parse()方法支持的浏览器如下:

*   谷歌 Chrome 1 及以上版本
*   Internet Explorer 3 及以上版本
*   Mozilla Firefox 1 及以上版本
*   歌剧 3 及以上
*   Safari 1 及以上