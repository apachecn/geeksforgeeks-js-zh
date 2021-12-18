# 如何在 JavaScript 中展开深度为 n 的函数？

> 原文:[https://www . geesforgeks . org/how-to-uncarry-a-function-up-depth-n-in-JavaScript/](https://www.geeksforgeeks.org/how-to-uncurry-a-function-up-to-depth-n-in-javascript/)

下面的方法介绍了如何在 JavaScript 中展开深度为 n 的函数。取消传递函数是包装函数参数并一次传递所有参数的过程。未传递到深度 n 意味着我们在所有参数中只传递了 n 个参数。

这可以通过以下方法实现:

*   **使用 reduce()方法**
*   **使用循环法**

**使用 reduce()方法:** Reduce 方法用于对列表的所有元素应用操作并返回结果。它接受一个应用于所有元素的回调。要将参数切片到 n，我们使用 slice()方法。slice()方法从列表中提取部分元素。slice()获取起始索引和结束索引，直到我们想要提取的内容。如果不提供任何参数，起始索引默认为 0。我们可以提供到列表末尾的索引。

**示例:**

## java 描述语言

```
<script>
// Uncurry that unwrap function
let uncurry = (f, n) => (...args) => {

    // Function that apply function to all elements
    let func = f => a => a.reduce((l, m) => l(m), f)

    // If args are less than n return
    if (n > args.length)
        return " less args provide ";

    // Apply function up t n
    return func(f)(args.slice(0, n));
}

let n = 3;
// Function sum three values
const sum = x => y => z => x + y + z;
let t = uncurry(sum, n);
let ans = t(1, 2, 4, 5);

console.log(`Sum of ${n} args are ${ans}`);
</script>
```

**输出:**

```
Sum of 3 args are 7
```

**使用或-of 循环方法:**在此方法中，我们使用*进行-of 循环*。 *for-of 循环*用于迭代列表的所有元素。下面是该方法的实现:

*   定义 n 和 sum 函数，将所有提供的参数相加。
*   用和、n 和所有数字列表调用 uncurrry 函数。
*   uncurry 函数检查 n 是否大于参数，然后返回较少的参数。
*   否则，它会迭代整个参数，并对每个参数应用函数 sum。
*   在 for 循环中，我们计算迭代。当迭代等于 n 时，打破循环。
*   最后返回 f，它是所有传递元素的和。

**示例:**

## java 描述语言

```
<script>
// Sum function that we have to uncurry
const sum = x => y => z => x + y + z;

// Function that uncurry  function up-to
// n depth  with for loop
const uncurry = f => n => {
    let k = 0;

    return (...args) => {

        if (n > args.length) {
            return "n";
        }
        for (let arg of args) {

            if (k === n)
                break;
            k++
            f = f(arg);
        }
        return f
    };

}

// Creating uncurry function with sum function and 3 value
let n = 3;
const uncurried = uncurry(sum)(n);

let ans = uncurried(0, 1, 7, 2, 4);
console.log(`Sum of ${n} args is ${ans}`);
</script>
```

**输出:**

```
Sum of 3 args is 8
```