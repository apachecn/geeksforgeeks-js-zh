# JavaScript 标签声明

> 原文:[https://www.geeksforgeeks.org/javascript-label-statement/](https://www.geeksforgeeks.org/javascript-label-statement/)

**标签**关键字不是 JavaScript 中的保留关键字，但可以是任意字符串。由于 JavaScript 不包含 g *oto* 关键字，用户可以在标签语句中使用 **continue** 关键字。此外，用户可以使用 **break** 关键字终止循环/阻塞。您也可以在不定义标签的情况下使用 break 关键字，但它只会终止父循环/块。要使用 break 关键字从内部循环终止外部循环，用户需要定义标签。定义 label 语句应遵循以下语法。

**语法:**

```
Label:
    statement (loop or block of code)
```

**要使用的关键词:**

*   **标签:**一个唯一字符串，用于定义块或循环的名称。
*   **语句:**可以是循环，也可以是块。
*   **Break:** 用于终止循环或代码块。
*   **继续:**用于终止或从循环的当前迭代跳转。

**带有 for 循环的 Label 语句:**在本节中，用户将学习为多个循环分配唯一的标签。此外，我们将在多个循环中使用中断和继续关键字。以下示例将演示使用循环的标签的使用。

**示例 1:** 使用带有标记循环的 break 关键字。用户可以使用标签从内环终止外环。

## java 描述语言

```
<script>
var sum = 0, a = 1;

// Label for outer loop
outerloop: while (true) {
    a = 1;

    // Label for inner loop
    innerloop: while (a < 3) {
        sum += a;
        if (sum > 12) {

            // Break outer loop from inner loop
            break outerloop;
        }
        console.log("sum = " + sum);
        a++;
    }
}
</script>
```

**输出:**我们可以看到，当和变得大于 12 时，外环终止。

```
sum = 1
sum = 3
sum = 4
sum = 6
sum = 7
sum = 9
sum = 10
sum = 12
```

**示例 2:** 使用带有标记循环的 continue 关键字。用户可以使用标签从内部循环跳到外部循环。

## java 描述语言

```
<script>
var sum = 0, a = 1;

// Label for outerloop
outerloop: while (sum < 12) {
    a = 1;

      // Label for inner loop
      innerloop: while (a < 3) {
        sum += a;
        if (a === 2 && sum < 12) {
              // Jump to outer loop from inner loop
              continue outerloop;
        }
        console.log("sum = " + sum + " a = " + a);
        a++;
      }
}
</script>
```

**输出:**当‘a = 2 且求和<12’条件执行为真时，它不会打印和，因为我们正在使用‘continue’关键字终止内循环的迭代。当 if 语句内部的条件为真时，它将跳转到外部循环。

```
sum = 1 a = 1
sum = 4 a = 1
sum = 7 a = 1
sum = 10 a = 1
sum = 12 a = 2
```

**示例 3:** 使用带有代码块的 label 语句。用户可以使用 break 关键字终止标记块的执行。

## java 描述语言

```
<script>
blockOfCode: {
    console.log('This part will be executed');
    break blockOfCode;
    console.log('this part will not be executed');
}
console.log('out of the block');
</script>
```

**输出:**可以观察到 break 关键字后的代码没有执行

```
This part will be executed
out of the block
```