# JavaScript 中的可变阴影

> 原文:[https://www . geesforgeks . org/variable-shadowing-in-JavaScript/](https://www.geeksforgeeks.org/variable-shadowing-in-javascript/)

**块作用域:**要理解 JavaScript 中的阴影，我们需要先搞清楚作用域。在计算机编程语言中，**作用域**是程序的某个部分/区域，在那里定义的变量可以存在并且可以被识别，除此之外它不能被访问。在 JavaScript 中，**块**是由花括号{}定义的复合语句，用于将多条语句组合成一条语句，其中 JavaScript 只需要一条语句。所有可以在一个块内访问的变量和函数都被称为在该块范围内，因此称为**块范围。**

例如，*让*和*常量*变量存储在单独的内存空间中，因此称为块作用域，但是*变量*变量可以在块外访问，因为它存储在全局对象内存空间中，因此称为**全局作用域。**

**隐藏:**现在，当一个变量在某个定义在其外部作用域上的同名作用域中声明时，当我们从内部作用域调用该变量时，在内部作用域中分配给该变量的值就是将存储在内存空间中该变量中的值。这被称为**阴影或可变阴影**。在 JavaScript 中，*的引入让 ECMAScript 6 中的*和*常量*与块范围一起允许变量隐藏。

**示例:**

## java 描述语言

```
function func() {
    let a = 'Geeks';

    if (true) {
        let a = 'GeeksforGeeks';  // New value assigned
        console.log(a); 
    }

    console.log(a); 
func();
```

**输出:**

```
GeeksforGeeks
Geeks
```

**非法阴影:**现在，在阴影一个变量的时候，不要越过范围的边界，即我们可以通过*让*变量来阴影 *var* 变量，但不能反其道而行之。所以，如果我们试图通过 *var* 变量来隐藏*让*变量，就称为**非法隐藏**，就会给出*这样的错误“变量已经定义了。”*

**例:**

## Javascript

```
function func() {
    var a = 'Geeks';
    let b = 'Geeks;

    if (true) {
        let a = 'GeeksforGeeks'; // Legal Shadowing
        var b = 'Geeks'; // Illegal Shadowing
        console.log(a); // It will print 'GeeksforGeeks'
        console.log(b); // It will print error
    }
}
func();
```

**输出:**

```
Identifier 'b' has already been declared
```

**注意:**箭头函数也遵循相同的作用域和可变阴影规则。