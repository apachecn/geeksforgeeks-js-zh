# 什么是 JavaScript 中的变量作用域？

> 原文:[https://www . geesforgeks . org/什么是 javascript 中的变量范围/](https://www.geeksforgeeks.org/what-is-variable-scope-in-javascript/)

在本文中，我们将了解 JavaScript 的范围。范围管理变量的可用性，或者我们也可以说它决定了变量的可访问性。

**JavaScript 中范围的类型:**

*   块范围
*   功能范围
*   本地范围
*   全球范围

**块范围:**早期的 JavaScript 只有全局范围和函数范围。 [**让**](https://www.geeksforgeeks.org/javascript-let/) 和**[**const**](https://www.geeksforgeeks.org/javascript-const/)**是 ES6 引入的两个新的重要关键词，这两个关键词在 JavaScript 中提供了 Block Scope。ECMAScript (ES6) 2015 是对 JavaScript 的第二次重大修订。在{ }块内声明的变量不能从块外访问。****

*   ******let 关键字:******

    ******例:**这里不能用 x****

    ```
    **{
     let x = 2;
    }**
    ```

*   ******有关键词:T1******

    ******例:**这里可以用 x****

    ```
    **{
     var x = 2;
    }**
    ```

****用 *var* 关键字声明的变量不能有块范围，它们可以在{ }块内声明，并且可以从块外访问。****

******示例:******

## ****超文本标记语言****

```
**<!DOCTYPE html>
<html>

<body>
    <h2 style="color:green">GeeksforGeeks</h2>
    <script>
        function foo() {
            if (true) {
                var x = '1';    // Exist in function scope
                const y = '2';  // Exist in block scope
                let z = '3';    // Exist in block scope
            }
            console.log(x);
            console.log(y);
            console.log(z);
        }
        foo();
    </script>
</body>

</html>**
```

******输出(控制台中):******

```
**1
y is not defined**
```

******函数作用域:** JavaScript 有一个函数作用域，每个函数创建一个新的作用域。函数内部定义的变量不能从函数外部访问，用 **var** 、 **let** 和 **const** 声明的变量在函数内部声明时非常相似。****

*   ******有关键词:T1******

    ******示例:******

    ```
    **function myFunction() {
       var firstName = "Krishna";   // Function Scope
    }**
    ```

*   ******let 关键字:******

    ******示例:******

    ```
    **function myFunction() {
      let firstName = "Krishna";   // Function Scope
    }**
    ```

*   ******const 关键字:******

    ******示例:******

    ```
    **function myFunction() {
       let firstName = "Krishna";   // Function Scope
    }**
    ```

******局部作用域:**函数内部声明的变量成为函数的局部变量。局部变量在函数启动时创建，在函数执行时删除。局部变量有函数作用域，这意味着它们只能从函数内部访问。****

******示例:******

```
**// This part of code cannot use firstName

function myFunction() {
 let firstName = "Krishna";
 // This part of code can use firstName
}

This part of code cannot use firstName**
```

## ****超文本标记语言****

```
**<!DOCTYPE html>
<html>

<body>
    <h2 style="color:green">
        GeeksforGeeks
    </h2>

    <script>
        function foo() {
            var x = '1';
            console.log('inside function: ', x);
        }

        foo();          // Inside function: 1
        console.log(x); // Error: x is not defined 
    </script>
</body>

</html>**
```

******输出(控制台中):******

```
**inside function: 1
x is not defined**
```

******全局作用域:**全局声明的变量(在任何函数之外)具有全局作用域，可以从程序中的任何地方访问全局变量。类似于用 **var** 、 **let** 和 **const** 声明的函数范围变量，在块外声明时非常相似。****

*   ******let 关键字:******

    ```
    **let x = 2;       // Global scope**
    ```

*   ******const 关键字:******

    ```
    **const x = 2;     // Global scope**
    ```

*   ******有关键词:T1******

    ```
    **var x = 2;       // Global scope**
    ```

******示例:******

## ****超文本标记语言****

```
**<!DOCTYPE html>
<html>

<body>
    <h2 style="color:green">GeeksforGeeks</h2>
    <script>

        // Global scope
        var x = '1'
        const y = '2'
        let z = '3'

        console.log(x);    // 1
        console.log(y);    // 2
        console.log(z);    // 3

        function getNo() {
            console.log(x);   // x is accessible here
            console.log(y);   // y is accessible here
            console.log(z);   // z is accessible here
        }
        getNo();           // 1
    </script>
</body>

</html>**
```

******输出(控制台中):******

```
 ****1**
 **2**
 **3**
 **1**
 **2**
 **3****
```