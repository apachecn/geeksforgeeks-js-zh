# JavaScript 类型错误–“X”不可重复

> 原文:[https://www . geesforgeks . org/JavaScript-type error-x-is-not-iteratable/](https://www.geeksforgeeks.org/javascript-typeerror-x-is-not-iterable/)

如果出现在函数(如 Promise.all 或 TypedArray.from)的 for…右侧或作为其参数的值不能迭代或不是可迭代对象，则会出现此 JavaScript 异常**不可迭代**。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**在代码中的某个地方，出现在 for…右侧的值，或者作为 Promise.all 或 TypedArray.from 等函数的参数，就像它可以迭代一样使用，或者是一个可迭代的对象。

**示例 1:** 在此示例中，GFG_Obj 不可迭代，因此出现了错误。

## HTML

```
<script>
    var GFG_Obj = { 'prop1': 'val1', 'prop2': 'val2' };
    // TypeError: GFG_Obj is not iterable
    for (let x of GFG_Obj) { 
        // Do Anything.
    }
</script>
```

**输出(控制台):**

```
TypeError: GFG_Obj is not iterable

```

**示例 2:** 在此示例中，GFG 不可迭代，因此出现了错误。

## HTML

```
<script>
    function* GFG(a, b) {
      yield a;
      yield b;
    }
    // TypeError: GFG is not iterable
    for (let y of GFG) 
        console.log(x);
</script>
```

**输出(控制台):**

```
TypeError: GFG is not iterable

```