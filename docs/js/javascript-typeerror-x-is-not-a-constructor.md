# JavaScript TypeError–“X”不是构造函数

> 原文:[https://www . geesforgeks . org/JavaScript-type error-x-is-not-a-constructor/](https://www.geeksforgeeks.org/javascript-typeerror-x-is-not-a-constructor/)

这个 JavaScript 异常**不是构造函数**，如果代码试图使用一个对象或变量作为构造函数，而该对象或变量不是构造函数，就会出现这个异常。

**消息:**

```
TypeError: Object doesn't support this action (Edge)
TypeError: "x" is not a constructor

TypeError: Math is not a constructor
TypeError: JSON is not a constructor
TypeError: Symbol is not a constructor
TypeError: Reflect is not a constructor
TypeError: Intl is not a constructor
TypeError: Atomics is not a constructor

```

**错误类型:**

```
TypeError

```

**错误原因:**代码试图在某个地方使用对象或变量作为构造函数，而该构造函数不是构造函数。

**示例 1:** 在本例中，变量(' var2 ')是一个字符串，用作构造函数，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Type Error</title>
</head>
<body>
    <script>
    var var2 = "This is string";
    document.write(new var2());
    </script>
</body>
</html>
```

**输出(在边缘控制台):**

```
TypeError: Object doesn't support this action

```

**例 2:** 本例中，Math 作为构造函数，所以出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Type Error</title>
</head>
<body>
    <script>
    document.write(new Math());
    </script>
</body>
</html>
```

**输出(在边缘控制台):**

```
TypeError: Object doesn't support this action

```