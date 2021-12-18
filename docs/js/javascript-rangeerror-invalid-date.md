# JavaScript range error–invalid date

> 哎哎哎:# t0]https://www . geeksforgeeks . org/JavaScript-range error-invalid-date/

如果提供给 **Date** 或 **Date.parse()** 的字符串无效，则会出现此 JavaScript 异常**无效日期**。

**消息:**T0】

**错误类型:**

```
RangeError

```

**错误原因:**在代码中为 **Date** 或 **Date.parse()** 方法提供了无效的日期字符串。

**示例 1:** 在此示例中，提供了无效字符串，因此出现了错误。

## HTML

```
<script>
new Date('2014-55-26').toISOString();
</script>
```

**输出(控制台中):**

```
RangeError: invalid time value

```

**示例 2:** 在此示例中，提供了无效字符串，因此出现了错误。

## HTML

```
<script>
var date = new Date('2020-57-16'); // Error here
date.toISOString();
</script>
```

**输出(控制台中):**

```
RangeError: invalid time value

```