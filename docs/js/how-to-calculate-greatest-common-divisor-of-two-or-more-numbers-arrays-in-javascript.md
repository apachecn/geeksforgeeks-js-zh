# 如何在 JavaScript 中计算两个或两个以上数字/数组的最大公约数？

> 原文:[https://www . geesforgeks . org/如何计算两个或更多数字的最大公约数-javascript 中的数组/](https://www.geeksforgeeks.org/how-to-calculate-greatest-common-divisor-of-two-or-more-numbers-arrays-in-javascript/)

给定两个或多个数字/数字数组，任务是在 JavaScript 中找到给定数字/数组元素的 GCD。

**例:**

```
Input  : arr[] = {1, 2, 3}
Output : 1

Input  : arr[] = {2, 4, 6, 8}
Output : 2
```

三个或三个以上数的 GCD 等于所有数共有的质因数的乘积，但也可以通过重复取数对的 GCD 来计算。

```
gcd(a, b, c) = gcd(a, gcd(b, c))
            = gcd(gcd(a, b), c)
            = gcd(gcd(a, c), b)
```

对于元素数组，我们执行以下操作。我们还将检查结果，如果任何一步的结果变成 1，我们将返回 1 作为 gcd(1，x) = 1。

```
result = arr[0]
For i = 1 to n-1
  result = GCD(result, arr[i])
```

下面是上述方法的实现。

**代码示例:**

## Javascript

```
<script>

    // Function to return gcd of a and b
    function gcd(a, b) {
        if (a == 0)
            return b;
        return gcd(b % a, a);
    }

    // Function to find gcd of array
    // of numbers
    function findGCD(arr, n) {
        let result = arr[0];
        for (let i = 1; i < n; i++) {
            result = gcd(arr[i], result);

            if (result == 1) {
                return 1;
            }
        }
        return result;
    }

    // Driver code
    let arr = [2, 4, 6, 8, 16];
    let n = arr.length;
    document.write(findGCD(arr, n) + "<br>");

</script>
```

**输出:**

```
2
```

**时间复杂度** : O(N * log(M))，其中 M 是数组的最小元素，N 是数组的长度。