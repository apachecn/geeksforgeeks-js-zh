# 如何在 ES6 中设置默认参数？

> 原文:[https://www . geesforgeks . org/如何设置默认参数 in-es6/](https://www.geeksforgeeks.org/how-to-set-default-parameters-in-es6/)

如果带有默认值的函数参数不包含任何值或未定义，则使用默认值进行初始化。默认情况下，JavaScript 函数参数被定义为未定义。但是，设置不同的默认值可能会很有用。这就是默认参数发挥作用的地方。

**语法:**

```
function name(parameter=value,...parameters) {

}
```

**例 1:** 如果我们在这个例子中相乘两个数字而不传递第二个参数，也不使用默认参数，这个函数返回的答案是 NAN(不是数字)，因为如果我们不传递第二个参数，这个函数会将第一个数字乘以 undefined。

## 超文本标记语言

```
<script>
    function multiply(a, b) {
        return a * b;
    }

    let num1 = multiply(5);
    console.log(num1);
    let num2 = multiply(5, 8);
    console.log(num2);
</script>
```

**输出:**

```
NaN
40
```

**例 2:** 如果我们不传一个数作为第二个参数，取默认参数作为第二个参数，它会把第一个数乘以默认数，如果我们传两个数作为参数，它会把第一个数乘以第二个数。

## 超文本标记语言

```
<script>
    function multiply(a, b = 2) {
        return a * b;
    }

    let num1 = multiply(5);
    console.log(num1);
    let num2 = multiply(5, 8);
    console.log(num2);
</script>
```

**输出:**

```
10
40
```

**例 3:** 带构造函数的缺省参数:我们可以将缺省参数概念用于一个类的构造函数。

## 超文本标记语言

```
<script>
    class Geeks {
        constructor(a, b = 3) {
            console.log(a * b);
        }
    }
    let obj = new Geeks(5);
    let obj1 = new Geeks(5, 4);
</script>
```

**输出:**

```
15
20
```