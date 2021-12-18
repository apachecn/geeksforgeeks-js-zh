# JavaScript type error–“X”为只读

> 原文:[https://www . geesforgeks . org/JavaScript-type error-x-is-只读/](https://www.geeksforgeeks.org/javascript-typeerror-x-is-read-only/)

这个 JavaScript 异常**是只读的**仅在严格模式下工作，如果分配给某个值的全局变量或对象属性是只读属性，就会出现这个异常。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**已赋值的全局变量或对象属性是只读属性。您不能在这些变量中写入数据。

**例 1:** 在本例中，不能修改 GFG_Obj 的任何属性。

## HTML

```
<script>
'use strict';
var GFG_Obj = Object.freeze({prop1: 'val1', prop2: 'val2'});
GFG_Obj.prop2 = 0;  // TypeError
</script>
```

**输出(控制台):**

```
TypeError: Assignment to read-only properties is not allowed in strict mode

```

**例 2:** 在本例中，数学的值。PI 不能更改(只读)。

## HTML

```
<script>
    'use strict';
    Math.PI = 5;
</script>
```

**输出(控制台):**

```
TypeError: Assignment to read-only properties is not allowed in strict mode

```