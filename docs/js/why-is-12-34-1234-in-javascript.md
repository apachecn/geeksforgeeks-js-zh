# 为什么 JavaScript 中的[1，2] + [3，4]=“1，23，4”？

> 原文:[https://www . geesforgeks . org/why-is-12-34-1234-in-JavaScript/](https://www.geeksforgeeks.org/why-is-12-34-1234-in-javascript/)

我们给出了一个表达式**【1，2】+【3，4】**，这个表达式的结果是**“1，23，4”。**在这篇文章中，我们将知道为什么会得到这个怪异的结果。

**示例:**

```
=> [1,2] + [3,4] 
=> "1,23,4"

=> [1, 2, 3, 4] + [9, 8]
=> "1, 2, 3, 49, 8"

=> [4] + []
=> "4"

=> [] + []
=> ""
```

在了解原因之前，我们先了解加法运算符(+)及其不同数据类型的结果。我们知道 javascript 中有 6 种内置数据类型**数字、字符串、对象、布尔、未定义**和**空**。而不同种类的数据类型相加的结果是不同的。

**例如:****未定义+未定义= >数，未定义+对象= >串**等。

在下表中所有相加的结果都给出了

<figure class="table">T14**布尔**T18**数字**T22**字符串**T26**对象**T30T32**未定义** 号号号号号号号号号号号号号号 弦弦弦弦弦弦弦弦弦弦弦弦弦

|  | is not defined. | T11】空 |
| number | number | number | strand | strand |
| No. **No.** | number | number | number | number | bowstring | bowstring | bowstring |
| String **string** string | bowstring | bowstring | bowstring | bowstring | bowstring | bowstring |

</figure>

**示例:**示例是通过这个简单的 JavaScript 程序获取该表的方法。

## java 描述语言

```
<script>
    let arr1 = [undefined, null, 1, "", {}];
    let arr2 = [undefined, null, 1, "", {}];

    for (var i = 0; i < arr1.length; i++) {
        arr2.map((item) => {
            console.log(typeof (arr1[i] + item));
        });
        console.log("\n\n");
    }
</script>
```

**输出:**在上面的程序中，有两个数组，其中提供了所有 6 个数据类型值。我们将 arr1 的每一项与 arr2 的每一项相加，并打印结果的类型。这就是我们创建上表的方式。
T3】

现在来看我们的问题**【1，2】+【3，4】**，这里我们是添加两个数组我们知道**数组**的类型是一个**对象**，那么根据上表当我们添加两个**对象**的时候就得到**字符串**类型的结果。JavaScript 将这两个数组转换成一个**字符串**，然后**连接**它们。这里两个数组都变成了**“1，2”**和**“3，4”**，当这两个字符串连接在一起时，我们得到**“1，23，4”**