# JavaScript type error–无法分配给“Y”上的属性“X”:不是对象

> 原文:[https://www . geesforgeks . org/JavaScript-type error-cant-assign-to-property-x-on-y-not-object/](https://www.geeksforgeeks.org/javascript-typeerror-cant-assign-to-property-x-on-y-not-an-object/)

这个 JavaScript 异常**不能分配给属性**仅在严格模式下发生，如果用户试图在任何一个原始值上创建属性，如符号、字符串、数字或布尔值，就会出现这个错误。原始值不能用于保存任何属性。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**在严格模式下，代码中的一个基元值用于在其上创建一个属性。原始值不能保存属性。

**示例 1:** 在本例中，字符串用于在其上创建属性，因此出现了错误。

## HTML

```
<script>
    'use strict';
    var GFG = "This is GeeksforGeeks";
    GFG.prop = {}; // error here
</script>
```

**输出(控制台):**

```
TypeError: Cannot create property 'prop' on string 
'This is GeeksforGeeks'

```

**示例 2:** 在本例中，布尔“true”用于在其上创建属性，因此出现了错误。

## HTML

```
<script>
    'use strict';
    var variableName = true;
    variableName.prop = {}; // error here
</script>
```

**输出(控制台):**

```
TypeError: Cannot create property 'prop' on boolean 'true'

```