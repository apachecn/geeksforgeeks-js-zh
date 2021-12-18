# 如何解决质数上 JavaScript 堆内存不足的问题？

> 原文:[https://www . geesforgeks . org/how-solution-JavaScript-堆内存不足在质数上/](https://www.geeksforgeeks.org/how-to-solve-javascript-heap-out-of-memory-on-prime-number/)

JavaScript 是一种高级的、动态类型的面向对象编程语言。当程序超过可用内存并导致溢出时，会引发“内存不足”错误。这也可能是由于对象太长或需要的内存大于分配的内存所致。由于 JavaScript 中的一切都是对象，对象都存储在堆中，所以我们在执行 JavaScript 程序时经常会遇到“堆内存不足”的错误。

让我们举一个非常常见的例子，一个程序决定了一个大数目的质因数，比如说 10^9 序。克服内存泄漏问题的方法是使用一种算法，该算法不需要循环遍历数字的末尾来找到质因数。

**算法:**函数 **primeFactors()** 接受一个参数 *num* ，它是要进行因子分解的原始数字。声明一个空数组来存储质因数。回路的外部*从 *i=2* 循环至 *i=sqrt(num)* 。如果数字除以 *i* 的当前值，则 *i* 的当前值被推入数组。因为我们只关心寻找不同的质因数，所以我们首先将该因数推入数组，然后继续用 *i* 除该数，直到它不能再被除为止，然后它打破*而*循环，减少 *num* 的值。*循环的*完成，检查*数值*的最终值。如果 *num* 的值大于 2，则它是最大的质因数，并被推入数组。*

**例 1:**

## java 描述语言

```
function primeFactors(num) {
    var prime = [];
    for (i = 2; i * i <= num; ++i) {
        if (num % i === 0) {

            // Prime factor found 
            prime.push(i);
            while (num % i === 0) {
                num /= i;
            }
        }
    }
    if (num > 2) {

        // Largest prime factor
        prime.push(num);
    }
    return prime;
}

console.log(primeFactors(992474117));
```

**输出:**

```
[ 23719, 41843 ]

```

**总结:**

1.  num = 99247117
2.  声明了质数数组
3.  对于从 *i=2* 到 *i=31503* 的循环运行
4.  *i=23719* 用 *rem=0* 除 *num* ，23719 也是素数，
    因此被推入数组。
5.  *num/i = 41843* 因此 *num= 41843* ，也是在 *i* 范围内不能被任何数
    整除的素数
6.  *num > 2* 并且是最大的质因数，因此它被推入数组。

**例 2:**

## java 描述语言

```
function primeFactors(num) {
    var prime = [];
    for (i = 2; i * i <= num; ++i) {
        if (num % i === 0) {
            // prime factor found
            prime.push(i);
            while (num % i === 0) {
                num /= i;
            }
        }
    }
    if (num > 2) {

        //largest prime factor
        prime.push(num);
    }
    return prime;
}
console.log(primeFactors(1000000000000000000));
```

**输出:**

```
[ 2, 5 ]

```

**总结:**

1.  *num = 100000000000000000000*为偶数，可被 2 整除。
2.  2 被推入数组，我们继续将 *num* 的当前值除以 2，直到它不再可分。
3.  循环通过 *i* 的范围，下一个质数是 5，被推入数组。
4.  完成循环的*后*数=0* 并且所有质因数都已存储。*