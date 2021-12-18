# JavaScript 中 var、let 和 const 关键字的区别

> 原文:[https://www . geesforgeks . org/var-let-and-const-keywords-in-JavaScript/](https://www.geeksforgeeks.org/difference-between-var-let-and-const-keywords-in-javascript/)之间的差异

在 [JavaScript](https://www.geeksforgeeks.org/javascript-tutorial/) 中，用户可以使用 3 个关键字来声明一个变量，这 3 个关键字是 [var、let 和 const](https://www.geeksforgeeks.org/how-to-declare-variables-in-different-ways-in-javascript/) 。在本文中，我们将看到 var、let 和 const 关键字之间的差异。我们将讨论每个关键词的范围和其他必要的概念。

**JavaScript 中的 var 关键字:***var*是 JavaScript 中声明变量最古老的关键字。

**作用域:**全局作用域或函数作用域。 *var* 关键字的范围是全局或函数范围。这意味着函数外部定义的变量可以全局访问，特定函数内部定义的变量可以在函数内部访问。

**例 1:** 变量‘a’是全局声明的。因此，变量“a”的范围是全局的，它可以在程序中的任何地方访问。显示的输出在控制台中。

## java 描述语言

```
<script>
    var a = 10
        function f(){
            console.log(a) 
        }
    f();
    console.log(a);
</script>
```

**输出:**

```
10
10
```

**示例 2:** 变量“a”在函数内部声明。如果用户试图在函数外访问它，它将消除错误。用户可以使用 *var* 关键字声明同名的两个变量。此外，用户可以将该值重新分配给 *var* 变量。控制台中显示的输出。

## Javascript

```
<script>
    function f() {

        // It can be accessible any
        // where within this function
        var a = 10;
        console.log(a)
    }
    f();

    // A cannot be accessible
    // outside of function
    console.log(a);
</script>
```

**输出:**

```
10
ReferenceError: a is not defined
```

**示例 3:** 用户可以使用 *var* 重新声明变量，用户可以更新 *var* 变量。输出显示在控制台中。

## Javascript

```
<script>  
    var a = 10

    // User can re-declare
    // variable using var
    var a = 8 

    // User can update var variable
    a = 7 
</script>
```

**输出:**

```
7
```

**示例 4:** 如果用户在声明前使用 var 变量，它将使用*未定义的*值进行初始化。输出显示在控制台中。

## Javascript

```
<script>
    console.log(a);
    var a = 10;
<script>
```

**输出:**

```
undefined
```

[**让**](https://www.geeksforgeeks.org/javascript-let/) **关键字在 JavaScript 中:**这个*让*关键字是 *var* 关键字的改进版。

**作用域:** [**块作用域:**](https://www.geeksforgeeks.org/javascript-es2015-block-scoping/) 一个*让*变量的作用域只是块作用域。它不能在特定块({block})之外访问。让我们看看下面的例子。

**示例 1:** 输出显示在控制台中。

## Javascript

```
<script>
    let a = 10;
    function f() {
        let b = 9
        console.log(b);
        console.log(a);
    }
    f();
</script>
```

**输出:**

```
9
10
```

**示例 2:** 代码返回一个错误，因为我们正在访问功能块外部的 *let* 变量。输出显示在控制台中。

## Javascript

```
<script>
    let a = 10;
    function f() {
        if (true) {
            let b = 9

            // It prints 9
            console.log(b);
        }

        // It gives error as it
        // defined in if block
        console.log(b);
    }
    f()

    // It prints 10
    console.log(a)
</script>
```