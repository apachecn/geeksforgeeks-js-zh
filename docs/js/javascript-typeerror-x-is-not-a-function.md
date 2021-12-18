# JavaScript TypeError–“X”不是函数

> 原文:[https://www . geesforgeks . org/JavaScript-type error-x-is-not-a-function/](https://www.geeksforgeeks.org/javascript-typeerror-x-is-not-a-function/)

这个 JavaScript 异常**并不是一个函数**，如果有人试图从一个函数中调用一个值，就会出现这个异常，但实际上，这个值并不是一个函数。

**消息:**

```
TypeError: Object doesn't support property or method {x} (Edge)
TypeError: "x" is not a function

```

**错误类型:**

```
TypeError

```

**错误原因:**试图从函数调用值，但实际上，该值不是函数。这里需要的是提供一个函数，但这并没有发生。

**示例 1:** 在本例中，document.getElementByID 用作函数，这不是。所以错误发生了。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Type Error</title>
</head>
<body>
    <script>
    let x = document.getElementByID('GFG');
    document.write(x);
    </script>
</body>
</html>
```

**输出(在 Chrome 控制台中):**

```
TypeError: document.getElementByID is not a function

```

**示例 2:** 在本例中，括号用作乘法，但它们类似于调用函数。所以错误发生了。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Type Error</title>
</head>
<body>
    <script>
    const x = 4(4 + 5);
    document.write(x);
    </script>
</body>
</html>
```

**输出(在 Chrome 控制台中):**

```
TypeError: 4 is not a function

```