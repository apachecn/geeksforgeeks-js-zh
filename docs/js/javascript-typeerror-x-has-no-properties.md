# JavaScript TypeError–“X”没有属性

> 原文:[https://www . geesforgeks . org/JavaScript-type error-x-has-no-properties/](https://www.geeksforgeeks.org/javascript-typeerror-x-has-no-properties/)

这个 JavaScript 异常**空(或未定义)没有属性**，如果试图访问空和未定义的属性，就会出现这个异常。他们没有任何这样的属性。

**消息:**

```
TypeError: Unable to get property {x} of undefined or null reference (Edge)
TypeError: null has no properties (Firefox)
TypeError: undefined has no properties (Firefox)

```

**错误类型:**

```
TypeError

```

**错误原因:**在某个地方，可以访问空或未定义的属性。

**示例 1:** 在本例中，变量(‘GFG’)被赋予了 **null** 值，并且它没有任何属性，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Type Error</title>
</head>
<body>
    <script>
    var GFG = null;
    document.write(GFG.prop_name);
    </script>
</body>
</html>
```

**输出(在边缘控制台):**

```
TypeError: Unable to get property 'prop_name' of 
undefined or null reference

```

**例 2:** 在本例中，变量(' var_name ')被赋予了**未定义的**值，它没有任何属性，因此出现了错误。

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
    document.write(var_name.prop_name);
    </script>
</body>
</html>
```

**输出(在边缘控制台):**

```
TypeError:Unable to get property 'prop_name' of 
undefined or null reference

```