# JavaScript SyntaxError–“使用严格”在带有非简单参数的函数中是不允许的

> 原文:[https://www . geesforgeks . org/JavaScript-syntaxerror-use-strict-不允许在函数中使用非简单参数/](https://www.geeksforgeeks.org/javascript-syntaxerror-use-strict-not-allowed-in-function-with-non-simple-parameters/)

如果在带有默认参数、rest 参数或析构参数的函数的开头使用了严格模式“use strict”语句，则在函数中不允许出现此 JavaScript 异常**“use strict”。**

**消息:**T0】

**错误类型:**

```
SyntaxError

```

**错误原因:**严格模式“使用严格”写在具有默认、静止或析构参数的函数的开始。

**例 1:** 在本例中，没有使用默认参数，所以没有出现错误。

## HTML

```
<script> 
  function GFG(a, b) {
            'use strict';
            return a + b;
    } 
  document.write(GFG(2, 5)); 
</script>
```

**输出:**

```
7

```

**示例 2:** 在本例中，使用了默认参数，因此出现了错误。

## HTML

```
<script> 
  function GFG(a=2, b=3) {
            'use strict';
            return a + b;
    } 
  document.write(GFG(2, 5)); 
</script>
```

**输出(控制台中):**

```
SyntaxError: Illegal 'use strict' directive in
function with non-simple parameter list

```