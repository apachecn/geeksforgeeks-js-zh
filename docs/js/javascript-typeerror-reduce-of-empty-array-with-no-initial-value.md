# JavaScript 类型错误–减少没有初始值的空数组

> 原文:[https://www . geeksforgeeks . org/JavaScript-type error-减空无初始值数组/](https://www.geeksforgeeks.org/javascript-typeerror-reduce-of-empty-array-with-no-initial-value/)

如果对空数组使用 reduce 函数，将出现这个没有初始值的空数组的 JavaScript 异常 **reduce。**

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**

如果为 reduce()方法提供了空数组，则会引发此错误，因为在这种情况下无法返回初始值。

**示例 1:** 在此示例中，filter 方法移除所有元素，因此 reduce 方法适用于空数组，并出现错误。

## HTML

```
<script>
var arr = [1, 2, 3, 4, 5, 6];
arr.filter(x => x < 0)
    // This removes all elements
    .reduce((x, y) => x * y) // TypeError
</script>
```

**输出(控制台):**

```
TypeError: reduce of empty array with no initial value

```

**示例 2:** 在此示例中，列表中有意外数量的元素，这可能会导致问题。

## HTML

```
<script>
    var classNm = document.getElementsByClassName("ClassName");
    var GFG_list = 
        Array.prototype.reduce.call(classNm, (a, b) => a + ": " + b);
</script>
```

**输出(控制台):**

```
TypeError: reduce of empty array with no initial value

```