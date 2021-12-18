# ES6 |数组 forEach()方法

> 原文:[https://www.geeksforgeeks.org/es6-array-foreach-method/](https://www.geeksforgeeks.org/es6-array-foreach-method/)

当使用数组时，迭代数组的元素并操作它们是很普遍的。传统上，这可以使用 for、while 或 do-while 循环来完成。forEach 将为数组中的每个元素调用函数。

**语法:**

```
array.forEach( callback, thisObject )
```

**参数:**该方法只接受上面提到和下面描述的两个参数:

*   **回调:**这允许函数测试数组中的每个元素。
*   **thisObject:** 执行回调函数时会调用这个。

**返回:**返回新创建的数组。
**不带 forEach()循环:**第一行用值[2，3，4，5，6]声明并初始化一个名为 array_1 的数字数组。为了使这个数组的每个元素都加倍，使用了一个 for 循环，它从零(因为数组的索引从零开始)到比数组长度小一的值。现在在第三行，从数组中提取每个元素，然后乘以 2，因此值会翻倍。
**程序 1:**

## java 描述语言

```
<script>
var array_1 = [2, 3, 4, 5, 6];
for(var i = 0; i < array_1.length; i++) {
    array_1[i] *= 2;
}
document.write(array_1);
</script>
```

**输出:**

```
4, 6, 8, 10, 12
```

**带 forEach()循环:**在 ES6 中，为数组引入了一种更容易理解和使用的方法，即 forEach()。让我们看看它是如何在上述情况下工作的。
T3】节目 2:

## java 描述语言

```
<script>
var array_1 = [2, 3, 4, 5, 6];
array_1.forEach(function(number, i) {
    array_1[i] *= 2;
});

document.write(array_1);
</script>
```

**输出:**

```
4, 6, 8, 10, 12
```

和前面一样，第一行声明并初始化一个名为 array_1 的数字数组，值为[2，3，4，5，6]。然后在 array_1 上调用 forEach 方法，该方法迭代数组并以回调函数作为参数。现在回调函数接受三个参数，

*   currentValue–这是必需的参数，对应于当前元素的值。
*   index–它是一个可选参数，这是当前元素的对应索引值。
*   array–它也是一个可选参数，这是原始数组，这里是 array_1。

因此，我们使用第二个参数，即 index，并遵循与之前完全相同的算法来使值翻倍。
**程序 3:** 这里我们只使用 currentValue 参数，使用该参数我们将名称数组中的每个值打印到控制台。

## java 描述语言

```
<script>
var names = ['Arpan', 'Abhishek', 'GeeksforGeeks'];

names.forEach(function(name){
    document.write(name + "<br/>");
});
</script>
```

**输出:**

```
Arpan
Abhishek
GeeksforGeeks
```