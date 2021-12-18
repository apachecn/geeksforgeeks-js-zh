# JavaScript 类型错误–无效数组.原型.排序参数

> 原文:[https://www . geesforgeks . org/JavaScript-type error-invalid-array-prototype-sort-argument/](https://www.geeksforgeeks.org/javascript-typeerror-invalid-array-prototype-sort-argument/)

如果 **Array.prototype.sort()** 的参数不是来自未定义的或相应排序的函数，则会出现此 JavaScript 异常**无效的 Array.prototype.sort 参数**。

**消息:**T0】

**错误类型:**

```
TypeError
```

**错误原因:**传递给 **sort()方法的参数**应该是未定义的或者是比较其操作数的函数。

**示例 1:** 在本例中，传递给 sort()方法的参数不是预期的，因此出现了错误。

## HTML

```
<script>
[2, 5, 6, 1, 3].sort(3); // error here
</script>
```

**输出:**

```
TypeError: argument is not a function object
```

**示例 2:** 在本例中，传递给 sort()方法的参数不是预期的，因此出现了错误。

## HTML

```
<script>
var compareFun = { 
    Asc: (a, b) => a >= b, 
    Dsc: (a, b) => a <= b 
};

// TypeError
[1, 2, 3, 6, 5, 8].sort(
    compareFun[this.key] || 'Asc');
</script>
```

**输出:**

```
TypeError: argument is not a function object
```