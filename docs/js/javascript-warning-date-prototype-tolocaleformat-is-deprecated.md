# JavaScript 警告–日期.原型. toLocaleFormat 不推荐使用

> 原文:[https://www . geesforgeks . org/JavaScript-warning-date-prototype-tolocaleformat-is-弃用/](https://www.geeksforgeeks.org/javascript-warning-date-prototype-tolocaleformat-is-deprecated/)

这个 JavaScript 警告**date . prototype . tolocaleformat 不推荐使用；考虑使用 Intl。如果用户使用非标准的 Date.prototype.toLocaleFormat 方法，则会出现日期时间格式。**

**消息:**T0】

**错误类型:**

```
Warning. JavaScript execution won't be halted.
```

**发生了什么？**

在代码中，使用了非标准的 Date.prototype.toLocaleFormat 方法，但它被折旧。

**例 1:** 在本例中，使用折旧法。所以错误发生了。

```
<script>
  var day = new Date(); 
  var date = day.toLocaleFormat('%B, %e. %A %Y'); // Warning here
</script>
```

**输出:**

```
Warning: Date.prototype.toLocaleFormat is deprecated; consider using Intl.DateTimeFormat instead

```

**例 2:** 在本例中，使用折旧法。所以错误发生了。

```
<script>
  var day = new Date();
  day.toLocaleFormat("%Y%m%d"); // Warning here
</script>
```

**输出:**

```
Warning: Date.prototype.toLocaleFormat is deprecated; consider using Intl.DateTimeFormat instead

```