# 如何在 JavaScript 中返回变量的数据类型？

> 原文:[https://www . geesforgeks . org/如何返回 javascript 中的数据类型变量/](https://www.geeksforgeeks.org/how-to-return-the-data-type-of-variable-in-javascript/)

在 JavaScript 中，与许多其他编程语言不同，我们在声明变量时不指定变量的类型，而是根据变量的值自动推断变量的类型。换句话说，JavaScript 是一种“动态类型化”的编程语言。在这种语言中，变量的类型可以在整个程序中改变。

**例**

## java 描述语言

```
<script>

    // x is a number
    var x = 4242;
    console.log(x);

    // x is a string
    x = "GeeksforGeeks";
    console.log(x)

    // x is an object
    x = {
        k: 4245,
        a: "geeks"
    }; 
    console.log(x)
</script>
```

**输出:**

```
4242
GeeksforGeeks
{k: 4245, a: "geeks"}
```

如上例所示，x 被初始化为一个数字，然后我们将其初始化为一个字符串，然后是一个对象。这使得很难在整个程序中跟踪变量“x”的类型。

**type of:**type of 关键字有助于确定 Javascript 中变量的类型。由于 Javascript 是一种动态类型的编程语言，因此可以使用的**类型来查找变量类型。**

它可以在函数中用于检查变量的数据类型或检查变量是否已声明。

让我们考虑下面的例子来更好地理解这一点。

**例 1:**

## java 描述语言

```
<script>

    var x = 12345;
    console.log(typeof(x));

</script>
```

**输出:**

```
number
```

**例 2:**

## java 描述语言

```
<script>

    var x = "GeeksforGeeks";
    console.log(typeof(x));

</script>
```

**输出:**

```
string
```

**例 3:**

## java 描述语言

```
<script>

  var x = { k : 12, m : "geeky stuff"}
  console.log(typeof(x))
  console.log(typeof(x.k))
  console.log(typeof(x.m))
  console.log(typeof(x.s))

</script>
```

**输出:**

```
object
number
string
undefined
```

typeof 运算符的一个常见用途是确定变量类型，并在函数中相应地执行操作。

**示例:**

## java 描述语言

```
<script>
    function doX(x) {
        if (typeof(x) === "number") {
            console.log("x is a number")
        }
        if (typeof(x) === "string") {
            console.log("x is a string")
        }
        if (typeof(x) === "undefined") {
            console.log("x is undefined")
        }
    }

    doX(12)
    doX("hello gfg")
</script>
```

用数字和字符串作为参数调用上面的函数。

**输出:**

```
x is a number
x is a string
```

**类型的**运算符的另一个用途是在变量使用之前检查它是否被声明。

**示例:**

## java 描述语言

```
<script>
    function checkX(x) {
        if (typeof(x) === "undefined") {
            console.log(
    "x is undefined. Please declare it");
        } else {
            console.log("We can process x!")
        }
    }

    checkX()
    checkX("hello")
</script>
```

在不传递参数的情况下调用上述函数，并将字符串作为参数传递。

**输出:**

```
x is undefined. Please declare it
We can process x!
```

类型为的**的一个小警告是类型为(NaN)的返回一个数字。当我们将一个字符串与一个数字相乘时，我们得到 NaN，如下例所示。**

**示例:**

## java 描述语言

```
<script>
    var x = "hello"
    console.log(x)

    var y = 10
    console.log(y)

    z = x * y
    console.log(z)
    console.log(typeof(z))
</script>
```

**输出:**

```
hello
10
NaN
number
```