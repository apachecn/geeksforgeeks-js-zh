# JavaScript 余数(%)运算符

> 原文:[https://www . geesforgeks . org/JavaScript-余数-运算符/](https://www.geeksforgeeks.org/javascript-remainder-operator/)

余数运算符是 JavaScript，用于在一个操作数除以另一个操作数时获取剩余值。在某些语言中，%被认为是模。当两个操作数的符号不同时，模和余数的作用不同。

在 JavaScript 中，余数取被除数的符号，要取模((a % n) + n)，应该使用% n 而不是% n。

**语法**

```
remainder = var1 % var2
```

**示例 1:** 本示例返回正余数，在这种情况下，模和余数将相同，因为两个操作数都是正的。

## java 描述语言

```
<script>
    // Initializing variables
    var a =4
    var n = 2

    // Calculating remainder
    var rem = a%n

    // Calculating modulo
    var mod = ((a%n)+n)%n

    // Printing result
    console.log("Remainder is "+rem)
    console.log("Modulo is "+mod)
</script>
```

**输出:**

```
"Remainder is 0"
"Modulo is 0"
```

**例 2:** 由于被除数为负，本例返回负余数。

## java 描述语言

```
<script>
    // Initializing variables
    var a =-4
    var n = 2

    // Calculating remainder
    var rem = a%n

    // Calculating modulo
    var mod = ((a%n)+n)%n

    // Printing result
    console.log(rem)
    console.log(mod)
</script>
```

**输出:**

```
-0
0
```

**例 3:** 无穷大和 NaN 的余数

## java 描述语言

```
<script>
    // Both operands are NaN
    console.log(NaN%NaN)

    // Dividend is NaN
    console.log(NaN%2)

    // Dividend is Nan and Divisor is Infinity
    console.log(NaN%Infinity)

    // Dividend is Infinity and Divisor is NaN
    console.log(Infinity%NaN)

    // Both operands are Infinity
    console.log(Infinity%Infinity)

    // Dividend is infinity
    console.log(Infinity%5)
</script>
```

**输出:**

```
> NaN
> NaN
> NaN
> NaN
> NaN
> NaN
```