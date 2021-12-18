# JavaScript TypeError – 更低的 "X" （not） "Y"

> [https://www.geeksforgeeks.org/javascript-typeerror-x-is-not-y/](https://www.geeksforgeeks.org/javascript-typeerror-x-is-not-y/)

如果数据类型不是预期的，就会出现这个 JavaScript 异常 **X(不是)Y** 。意外的是未定义或空值。

**消息:**

```
TypeError: Unable to get property {x} of undefined or null reference (Edge)
TypeError: "x" is (not) "y" (Firefox)

Few example are given below:
TypeError: "x" is undefined
TypeError: "y" is null
TypeError: "undefined" is not an object
TypeError: "y" is not an object or null
TypeError: "x" is not a symbol

```

**错误类型:**

```
TypeError

```

**错误原因:**有一个意外的数据类型提供给任何一个方法，这需要其他东西。出现这种情况时，值未定义或为空。

**示例 1:** 在本例中，变量(' var_name ')未定义，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Type Error</title>
</head>
<body>
    <script>
    var var_name = undefined;
    document.write(var_name.substring(3));
    </script>
</body>
</html>
```

**输出(在边缘控制台):**

```
TypeError: Unable to get property 'substring' of undefined or null reference

```

**例 2:** 在本例中，变量(' var1 ')为空，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Type Error</title>
</head>
<body>
    <script>
    var var1 = null;
    document.write(var1.substring(3));
    </script>
</body>
</html>
```

**输出(在边缘控制台):**

```
TypeError: Unable to get property 'substring' of undefined or null reference

```