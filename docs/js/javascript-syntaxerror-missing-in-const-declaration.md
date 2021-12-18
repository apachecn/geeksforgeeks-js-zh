# JavaScript 语法错误–常量声明中缺少=号

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-missing-in-const-declaration/](https://www.geeksforgeeks.org/javascript-syntaxerror-missing-in-const-declaration/)

如果声明了一个常量并且没有提供值(比如 const ABC _ DEF).需要在同一语句中提供值(const ABC_DEF = '#ee0 ')。

**消息:**

```
SyntaxError: Const must be initialized (Edge)
SyntaxError: missing = in const declaration (Firefox)
SyntaxError: Missing initializer in const declaration (Chrome)
```

**错误类型:**

```
SyntaxError
```

**错误原因:**程序在执行时不能更改常数值。也不能通过重新分配来改变。

**示例 1:** 在此示例中，声明了一个常量，但未初始化，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      const GFG;                 
      document.write(GFG);
    </script>
</body>
</html>
```

**输出:**

```
SyntaxError: Const must be initialized
```

**示例 2:** 在此示例中，稍后声明并初始化了一个常量，因此出现了错误。

## 超文本标记语言

```
<!DOCTYPE html>
<html>
<head>
    <title>Syntax Error</title>
</head>
<body>
    <script>
      const INIT_VAL;
      // invalid statement
      INIT_VAL = 5;                 
      document.write(INIT_VAL);
    </script>
</body>
</html>
```

**输出:**

```
SyntaxError: Const must be initialized
```