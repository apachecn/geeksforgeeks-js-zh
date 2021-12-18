# JavaScript 类型错误–无法删除不可配置的数组元素

> 原文:[https://www . geesforgeks . org/JavaScript-type error-cant-delete-不可配置-数组-元素/](https://www.geeksforgeeks.org/javascript-typeerror-cant-delete-non-configurable-array-element/)

这个 JavaScript 异常**不能删除不可配置的数组元素**，如果试图缩短数组长度，并且数组的任何一个元素都是不可配置的，就会出现这个异常。

**消息:**T0】

**错误类型:**

```
TypeError

```

**错误原因:**当数组的某个元素不可配置，代码试图缩短数组长度时。

**示例 1:** 在此示例中，数组属性不可配置，试图通过缩短数组长度来删除属性。

## HTML

```
<script>
    var array = [];
    Object.defineProperty(array, 1, {value: 4}); 
    Object.defineProperty(array, 2, {value: "4"});
    array.length = 1; // Error here
</script>
```

**输出:**

```
TypeError: can't delete non-configurable array element

```

**示例 2:** 在此示例中，数组属性不可配置，试图通过缩短数组长度来删除属性。

## HTML

```
<script>
    var array = ['a', 'b', 'c'];
    Object.seal(array);
    array.length = 1; // Error here
</script>
```

**输出:**

```
TypeError: can't delete non-configurable array element

```