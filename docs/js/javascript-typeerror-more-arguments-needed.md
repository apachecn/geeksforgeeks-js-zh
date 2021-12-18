# JavaScript 类型错误–需要更多参数

> 原文:[https://www . geesforgeks . org/JavaScript-type error-more-arguments-required/](https://www.geeksforgeeks.org/javascript-typeerror-more-arguments-needed/)

如果调用函数的方式有错误，就会出现这个 JavaScript 异常**需要更多的参数**。如果提供了一些参数，那么需要提供更多的参数。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**函数调用方式有错误。可能需要提供更多的参数。

**示例 1:** 在本例中，Object.create 至少需要 1 个参数，但没有传递任何内容，因此出现了错误。

## HTML

```
<script>
    // TypeError
    var GFG_Obj = Object.create(); 
</script>
```

**输出(控制台):**

```
TypeError: argument is not an Object and is not null

```

**示例 2:** 在本例中，Object.setPrototypeOf 至少需要 2 个参数，但只传递了 1 个，因此出现了错误。

## HTML

```
<script>
    var GFG_Obj = Object.setPrototypeOf({});
</script>
```

**输出:**

```
TypeError: argument is not an Object and is not null

```