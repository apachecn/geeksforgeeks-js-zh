# JavaScript 中的第一类函数是什么？

> 原文:[https://www . geesforgeks . org/什么是 javascript 中的一流函数/](https://www.geeksforgeeks.org/what-is-the-first-class-function-in-javascript/)

**一级函数:**如果一种编程语言中的函数被视为其他变量，则称该语言具有一级函数。因此，这些函数可以赋给任何其他变量，或者作为参数传递，或者由另一个函数返回。JavaScript 将函数视为一等公民。这意味着函数只是一个值，只是另一种类型的对象。

**举例:**我们举个例子，多了解一下一级函数。

## java 描述语言

```
<script>
    const Arithmetics = {
        add: (a, b) => {
            return `${a} + ${b} = ${a + b}`;
        },
        subtract: (a, b) => {
            return `${a} - ${b} = ${a - b}`
        },
        multiply: (a, b) => {
            return `${a} * ${b} = ${a * b}`
        },
        division: (a, b) => {
            if (b != 0) return `${a} / ${b} = ${a / b}`;
            return `Cannot Divide by Zero!!!`;
        }

    }

    document.write(Arithmetics.add(100, 100) + "<br>");
    document.write(Arithmetics.subtract(100, 7) + "<br>");
    document.write(Arithmetics.multiply(5, 5) + "<br>");
    document.write(Arithmetics.division(100, 5));
</script>
```

**注意:**在上面的例子中，函数作为变量存储在对象中。

**输出:**

```
100 + 100 = 200
100 - 7 = 93
5 * 5 = 25
100 / 5 = 20
```

**例 2:**

## java 描述语言

```
<script>
    const Geek = (a, b) => {
        return (a + " " + b);
    }

    document.write(Geek("Akshit", "Saxena"));
</script>
```

**输出:**

```
Akshit Saxena
```