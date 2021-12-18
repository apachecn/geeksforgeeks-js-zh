# JavaScript 语法错误–“x”不是合法的 ECMA-262 八进制常量

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-x-is-not-a-legal-ECMA-262-octal-constant/](https://www.geeksforgeeks.org/javascript-syntaxerror-x-is-not-a-legal-ecma-262-octal-constant/)

这个 JavaScript 警告 **08(或 09)不是一个合法的 ECMA-262 八进制常量**出现在文字 08 或 09 被用作数字的情况下。这是因为这些文字不能被视为八进制数。

**消息:**T0】

**错误类型:**

```
Warning. JavaScript execution won't be halted.

```

**错误原因:**当前导 0 后的任何数字等于或大于 8 时，就会出现这种情况。这个数字不能被视为八进制数，因此 JavaScript 会给出一个警告。

**例 1:** 在本例中，文字“08”给出警告，因为它不能解释为八进制数。

## HTML

```
<script>
"use strict";
// Error here
08;
</script>
```

**输出:**

```
Warning: SyntaxError: 08 is not a legal ECMA-262 octal constant.

```

**例 2:** 在本例中，文字“09”给出警告，因为它不能解释为八进制数。

## HTML

```
<script>
"use strict";
// Error here
09;
</script>
```

**输出:**

```
Warning: SyntaxError: 09 is not a legal ECMA-262 octal constant.

```