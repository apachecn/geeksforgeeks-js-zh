# JavaScript 中的 currying 函数是什么？

> 原文:[https://www . geesforgeks . org/what-is-curry-in-function-in-JavaScript/](https://www.geeksforgeeks.org/what-is-currying-function-in-javascript/)

它是函数编程中的一种技术，将多个参数的函数按顺序转换成单个参数的多个函数。
函数的翻译是这样发生的，

> 函数 simpleFunction(param1，param2，param3，…..)= >函数 curriefunction(param 1)(param 2)(param 3)(…。

我们简单地将函数包装在一个函数中，这意味着我们将从另一个函数返回一个函数来获得这种转换。父函数接受第一个提供的参数，并返回接受下一个参数的函数，这样一直重复，直到参数的数量结束。希望接收最后一个参数的函数返回预期的结果。

**注:**一位名叫哈斯克尔·库里的美国数学家发展了这种技术，这就是为什么它被称为 currying。

**例 1:** 假设我们有一个长方体的长、宽、高，我们要构造一个可以计算体积的函数。该函数被调用，随后通过提供的参数执行其代码并返回适当的结果，最后*控制台日志*在控制台上打印返回值。

## Java Script 语言

```
<script>
    function calculateVolume(length, breadth, height) {
        return length * breadth * height;
    }
    console.log(calculateVolume(4, 5, 6));
</script>
```

**输出:**

```
120
```

**例 2:** 这个例子借助闭包解释了 currying 技术。在执行的[线程期间，将调用*计算体积()*功能。里面有一个](https://www.geeksforgeeks.org/javascript-code-execution/)[匿名](https://www.geeksforgeeks.org/javascript-anonymous-functions/)函数，接收一个参数并返回一些代码。我们正在从另一个函数中暴露我们的函数，因此将创建[闭包](https://www.geeksforgeeks.org/closure-in-javascript/)。闭包总是包含函数定义和父元素的词法环境，两者作为一个包保持连接。因此，我们在哪里调用它们并不重要，所有内部函数都将始终保持对其父变量的访问。
一旦我们得到作为函数返回的结果，下一个参数就准备好被传递，这个过程将持续到第二个最后一个函数。最后，最里面的 return 关键字返回预期的结果。

## Java Script 语言

```
<script>
    function calculateVolume(length) {
        return function (breadth) {
            return function (height) {
                return length * breadth * height;
            }
        }
    }
    console.log(calculateVolume(4)(5)(6));
</script>
```

**输出:**

```
120
```