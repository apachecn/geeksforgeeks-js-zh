# 如何解决在 javaScript 中使用 performance.now()方法时出现的问题？

> 原文:[https://www . geeksforgeeks . org/如何解决在使用 javascript 中的性能即方法时出现的问题/](https://www.geeksforgeeks.org/how-to-solve-the-issue-that-arise-while-using-performance-now-method-in-javascript/)

任何一个程序员，只要有足够的时间，都可以解决一个问题，唯一重要的是。性能在软件中起着非常重要的作用。一个性能好的网站可以吸引更多的用户，而性能相对较差的网站则不能。随着 JavaScript 在制作非常大的网站项目中的使用日益增加，确保我们的代码快速非常重要。但是如何确保代码足够快呢！一般来说，在 JavaScript 中检查函数性能的最好方法是内置 **performance.now()** 方法。
为了衡量一个函数的性能，即一个函数需要多少时间来执行或计算运行时间， **performance.now()方法**被广泛使用。它返回自程序开始以来经过的时间。看看下面的问题陈述，这个概念会更清楚。
**例:**我们来看看遍历一个 10 万元素的数组需要多少时间。

*   **程序:**

## java 描述语言

```
<script>
/* Creating a massive array of 100000 elements*/
const array2 = new Array(100000).fill('Gfg');
const { performance } = require('perf_hooks');

/*Calculating the time time taken */
function calculatePerformance(array) {
    /*Before beginning the loop, calculating performance*/
    let t0 = performance.now();
    console.log(array)
    for (let i = 0; i < array.length; i++) {
        if (array[i] == 'Gfg') {
            console.log("Gfg is present in array");
        }
    }
    //Calculating performance after the loop is executed
    let t1 = performance.now();

    console.log("call to the above function took"
    + (t1 - t0) + "milliseconds");
}
calculatePerformance(array2);
</script>
```

*   **输出:**

```
call to the above function took1385.733816999942milliseconds
```

在上面的例子中，可以清楚地看到我们如何使用 **performance.now()** 来检查函数的运行速度。此外，此方法返回一个反映当前时间的浮点数，单位为毫秒(精确到千分之一毫秒)。这是一种测量函数性能的非常简单的技术。这个时间是不固定的，每次我们再次运行代码时，它可能会改变。随着数组中元素数量的增加，函数变得更慢，运行时间也增加。如果我们在不同的电脑上运行同一个程序会花费不同的时间，原因是 CPU。运行某项功能或执行某项任务所花费的时间取决于 CPU 的功能有多强大，以及特定计算机上正在运行哪些其他程序。
**performance . now():**这里会出现一个问题，因为如果两个人写了完全相同的代码，我们不能断定运行时间少的用户写了更好的代码。**大 O 符号**的需求来了。
**大 O 记数法:**大 O 是用来衡量不同功能的表现。对于同一个问题可以有不同的解决方案，但是在这些方案中，哪一个更好，效率更高。大 O 是这么说的。大 O 不会用秒来衡量事物。相反，它关注运行时在增加操作数量时增长的速度。它提供了计算函数性能的标准方法。
因此，对于上面的例子，即使运行时间可能因人而异，但为同一程序计算的大 O 对每个人来说都是相同的。因为算法的运行时间在相同大小的不同输入之间可能不同。我们使用 Big -O 来计算最坏情况下的时间复杂度，这是给定大小的输入所需的最大时间量。这就是我们计算不同函数大 O 的主要原因。
举一个解**魔方**的简单例子，在多少时间内解出来，要看人对人，一个人只需 30 秒就能解出来，另一个人可能需要几个小时才能解出来。我们可以定义最坏的情况，即一个人求解立方体所花费的最大时间。我们所说的情况也是如此，Big-O 给出了最坏的时间，我们可以用标准的方法来估计一个函数的性能。对于同样的问题陈述，如果我们计算大 O，它将是 O(n)。这意味着运行时间将随着输入的大小线性增加，输入中的操作数量越多，函数花费的时间就越多。Big-O 是一种更精确的性能计算方法，因为它给出了最坏的情况，即函数执行的最大时间。
**大 O 记数法求解:**通过查看给定的函数，可以看出在计算函数的运行时间时，数组的大小并不重要。该功能将在**0(1)**时间运行，也称为恒定时间。不管输入数组是由 1 项、100 项还是 1000 项组成，这个函数仍然只需要一个步骤。

1.  O(1)
2.  O(1)
3.  O(1)

因此，可以得出结论: **Big-O** 是一种更精确的性能计算方法，因为它给出了最坏的情况，即函数执行所需的最长时间，而且它给出了适用于所有其他同类函数的标准解决方案。