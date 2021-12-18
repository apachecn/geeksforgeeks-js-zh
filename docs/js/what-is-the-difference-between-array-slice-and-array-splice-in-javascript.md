# JavaScript 中 Array.slice()和 Array.splice()有什么区别？

> 原文:[https://www . geesforgeks . org/数组切片和数组拼接在 javascript 中的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-array-slice-and-array-splice-in-javascript/)

Javascript 数组是可以保存多个值的变量。有许多方法与这些数组相关联。slice()和 splice()方法是广泛使用的数组操作方法。下表列出了它们之间的不同之处。

| 切片() | 拼接() |
| 此方法用于通过选择给定数组的子数组来获取新数组。 | 此方法用于在给定数组中添加/移除项。 |
| 参数**‘T1’表示起始指数，**‘e’**表示结束指数。它们表示要获取的子阵列的索引。默认情况下，开始值为“0”，结束值为“n”。** | 参数**‘I’**表示起始索引，**‘n’**表示要从指定起始索引中删除的项目数。**'第一项，第二项，…..项目 n'** 表示在给定索引处添加的新项目列表。如果 n=0，则不删除任何项目，新项目只是添加到指定的起始索引。 |
| 更改不会反映在原始数组中。 | 这些变化反映在原始数组中 |
| 结果必须赋给一个新的数组变量。 | 结果不需要分配给任何其他新变量。 |
| 返回值是一个新数组，其值在给定数组的选定子数组中。将选择范围从开始到(结束-1)的值。 | 返回值是一个包含被删除元素的数组。 |
| 正好接受 2 个参数 | 接受“n”个参数(可以提供新项目列表) |

**语法:**

*   **切片():**T0】
*   **拼接():**T0】

**切片()方法示例**
**示例 1:** 指定了开始和结束。

```
<script>
    var cars=['Benz', 'Innova', 'Breeza', 'Etios', 'Dzire'];
    var new_cars=cars.slice(1, 4);
    document.write("cars :", cars, "<br><br>");
     document.write("new_cars :", new_cars);
</script>
```

**输出:**

```
cars :Benz, Innova, Breeza, Etios, Dzire
new_cars :Innova, Breeza, Etios
```

**例 2:** 只指定了开始。默认情况下，结尾是数组的长度。

```
<script>
    var cars=['Benz', 'Innova', 'Breeza', 'Etios', 'Dzire'];
    var new_cars=cars.slice(2);
    document.write("cars :", cars, "<br><br>");
    document.write("new_cars :", new_cars);
</script>
```

**输出:**

```
cars :Benz, Innova, Breeza, Etios, Dzire

new_cars :Breeza, Etios, Dzire
```

**拼接()方法示例**
**示例 1:** 现在让我们只添加一些项目，但不移除任何项目。

```
<script>
    var cars=['Benz', 'Innova', 'Breeza', 'Etios', 'Dzire'];
    cars.splice(2, 0, 'ambassedor', 'BMW', 'Audi');
    document.write("cars :", cars, "<br><br>");
</script>
```

**输出:**

```
cars :Benz, Innova, ambassedor, BMW, Audi, Breeza, Etios, Dzire
```

**示例 2:** 删除一个元素，不添加任何新项目

```
<script>
    var cars=[
'Benz', 'Innova', 'ambassedor', 'BMW', 'Audi', 'Breeza', 'Etios', 'Dzire'];
    cars.splice(2, 1);
    document.write("cars :", cars, "<br><br>");
</script>
```

**输出:**

```
cars :Benz, Innova, BMW, Audi, Breeza, Etios, Dzire

```

**示例 3:** 删除多个元素，不添加任何新项目。

```
<script>
    var cars=[
'Benz', 'Innova', 'ambassedor', 'BMW', 'Audi', 'Breeza', 'Etios', 'Dzire'];
    cars.splice(2, 3);
    document.write("cars :", cars, "<br><br>");
</script>
```

**输出:**

```
cars :Benz, Innova, Breeza, Etios, Dzire
```

删除多个元素时，在上述情况下，指定的起始索引为“2”，需要删除“3 元素”，因此它会开始从索引本身删除元素。因此，索引 2、3 和 4 中的项目被移除。