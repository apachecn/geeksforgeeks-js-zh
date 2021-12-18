# JavaScript 引用错误不推荐使用的调用者或参数用法

> 原文:[https://www . geesforgeks . org/JavaScript-reference error-弃用-调用者-或-参数-用法/](https://www.geeksforgeeks.org/javascript-referenceerror-deprecated-caller-or-arguments-usage/)

这个 JavaScript 异常**不推荐使用的调用者或参数用法**只在严格模式下出现。如果使用了**函数调用方**或**函数参数**属性中的任何一个，并且这些属性被折旧，就会出现这种情况。

**消息:**T0】

**错误类型:**

```
This is a strict-mode warning that a ReferenceError occurred. 
JavaScript execution won't be halted.

```

**错误原因:**在代码中，使用了 Function.caller 或 Function.arguments 属性，这些属性被折旧。

**示例 1:** 在此示例中，使用了调用者属性，因此出现了错误。

## HTML

```
<script>
'use strict';
function GFG_Fun() {
    return GFG_Fun.caller; // Error here
}
GFG_Fun();
</script>
```

**输出:**

```
TypeError: 'arguments', 'callee' and 'caller' are 
restricted function properties and cannot be accessed 
in this context

```

**示例 2:** 在此示例中，使用了 arguments 属性，因此出现了错误。

## HTML

```
<script>
'use strict';
function gfg(n) {
  return gfg.arguments[0]; // Error here
}
gfg(2);
</script>
```

**输出:**

```
TypeError: 'arguments', 'callee' and 'caller' are 
restricted function properties and cannot be accessed
in this context

```