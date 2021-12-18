# JavaScript 范围错误–重复计数必须为非负数

> 原文:[https://www . geesforgeks . org/JavaScript-range error-repeat-count-必须是非负数/](https://www.geeksforgeeks.org/javascript-rangeerror-repeat-count-must-be-non-negative/)

如果传递给**string . prototype . repeat()**方法的参数为负数，则出现此 JavaScript 异常**重复计数必须为非负数**。

**消息:**T0】

**错误类型:**

```
RangeError

```

**错误原因:**repeat()方法有一个参数，该参数指示字符串的重复次数。它应该在 0 到无穷大的范围内，并且不能是负数。

**示例 1:** 在此示例中，传递的参数值是负值，因此出现了错误。

## HTML

```
<script> 
    'GFG'.repeat(-1); // error here
</script>
```

**输出(控制台):**

```
RangeError: Invalid count value

```

**示例 2:** 在此示例中，传递的参数值是负值，因此出现了错误。

## HTML

```
<script> 
    var gfg = "This is GeeksforGeeks";
    gfg.repeat(-100); // error here
</script>
```

**输出(控制台):**

```
RangeError: Invalid count value

```