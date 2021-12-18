# 用 JavaScript 将一个数字四舍五入到 5 的下一个倍数

> 原文:[https://www . geesforgeks . org/round-off-a-number-to-next-倍数-5-使用 javascript/](https://www.geeksforgeeks.org/round-off-a-number-to-the-next-multiple-of-5-using-javascript/)

给定一个正整数 n，任务是将该数舍入到下一个可被 5 整除的整数。

**例:**

```
Input : 46 
Output : 50

Input : 21
Output : 25

Input : 30 
Output : 30

```

**方法 1:**

*   Take the number in the variable.
*   Divide by 5 to get the decimal value.
*   Use **math.ceil ()** to take the ceil value of decimal value.
*   Multiply by 5 to get the result.

```
<script>
    function round(x) {
        return Math.ceil(x / 5) * 5;
    }

var n = 34;
console.log(round(n)); 
</script>
```

**输出:**

```
35

```

**方法 2:**

*   Take the number in the variable.
*   If divisible by 5, the same number is returned.
*   Otherwise, divide by 5, take the floor value, multiply by 5, and add 5.

```
<script>
    function round(x) {
        if (x % 5 == 0) {
            return int(Math.floor(x / 5)) * 5;
        } else {
            return (int(Math.floor(x / 5)) * 5) + 5;
        }
    }

var n = 34;
console.log(round(n)); 
</script>
```

**输出:**

```
35

```