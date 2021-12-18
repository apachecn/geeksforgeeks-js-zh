# 什么是阻塞作用域变量 ES6？

> 原文:[https://www . geesforgeks . org/什么是阻塞作用域变量-es6/](https://www.geeksforgeeks.org/what-is-blocked-scoped-variables-es6/)

在 ES5 中，当我们用 **var** 关键字声明一个变量时，这个变量的范围要么是全局的，要么是局部的。
**全局变量:**当我们在函数外声明一个变量时。
**局部变量:**当我们在函数内部声明一个变量时。

但是，ECMAScript 2015 (ES6)引入了两个新的关键词**让**和 **const** 和**T5】这两个关键词在 JavaScript 中提供了 Block Scope。所有在花括号{ }中声明的变量都被限制只能在该块内和该块的块内访问。我们不能访问该块之外的变量，它要么通过一个 ReferenceError(变量未定义)，要么如果他在全局范围内有一个同名的变量，那么它将引用该变量。**

**let 关键字:**用 **var** 关键字声明的变量允许重新声明，但用 **let** 关键字声明的变量在**同一个区块**不允许重新声明。它将通过语法错误:标识符已经被声明。

**示例:**

## 超文本标记语言

```
<script>
    function valueAssign() {
        let x = 10;
        var z = 15;
        if (true) {
            let y = 5;
            console.log(y); // Here y is 5
            console.log(x); // Here x is 10
            console.log(z); // Here z is 15
        }
        console.log(x); // Here x is 10
        console.log(z); // Here z is 15
        console.log(y); // ReferenceError: y is not defined  
    }

    valueAssign();
</script>
```

**输出:**

```
5
10
15
10
15
ReferenceError: y is not defined
```

这里我们看到 x 和 z 都在外部块中声明，参考 if 的块{}和 y 在内部块中声明。这里 z 是用 var 关键字声明的，所以我们在这个 valueAssign()函数中处处使用 z 变量，因为用 var 关键字声明的变量不能有块范围。但是 x 和 y 都是用 let 关键字声明的。这里 x 在外块中声明，所以我们可以在内块中使用 x。因为 y 是在内部块中声明的，所以我们不能在外部块中使用它。Let 和 const 将处理我将要声明的块，并将处理其中的块。因此，当我们在外块中打印 y 时，它会给出一个错误。

**例 2:** 在本例中，我们将看到用 **var** 和 **let** 重新定义变量的工作过程:

## 超文本标记语言

```
<script>
    // Redeclared using var
    function valueAssignWithVar() {
        var y = 20;
        y = 30; // Redeclare allowed
        console.log(y);
    }

    // Redeclared using let in different block
    function valueAssignWithLet1() {
        let x = 20;
        if (true) {
            let x = 5; // Redeclare allowed
            console.log(x);
        }
        console.log(x);
    }

    // Redeclared using let in same block
    function valueAssignWithLet2() {
        let x = 10;
        let x = 5; // Redeclare not allowed

        // SyntaxError: Identifier 'x' has
        // already been declared
        console.log(x); 
    }

    valueAssignWithVar();
    valueAssignWithLet1();
    valueAssignWithLet2();
</script>
```

**输出:**

```
30
5
20
SyntaxError: Identifier 'x' has already been declared
```

**const 关键字**:用 **const** 关键字声明的变量严格不允许用**同一个块**重新声明和重新分配。当您不想在整个程序中更改变量的值时，我们使用 **const** 关键字。

**示例:**在本例中，我们将看到使用**常量**重新分配变量的工作

## 超文本标记语言

```
<script>
    // Reassigned not allowed
    const x = 10;
    x = 5; // TypeError: Assignment to constant variable
    console.log(x);
</script>
```

**输出:**

```
TypeError: Assignment to constant variable.
```

**示例 2:** 在本例中，我们将看到使用**常量**重新定义变量的工作

## 超文本标记语言

```
<script>
    // Redeclared using const in different block
    function valueAssignWithConst1() {
        const x = 20;
        if (true) {
            const x = 5; // Redeclare allowed
            console.log(x);
        }
        console.log(x);
    }

    // Redeclared using const in same block
    function valueAssignWithConst2() {
        const x = 10;
        const x = 5; // Redeclare not allowed

        // SyntaxError: Identifier 'x' has
        // already been declared
        console.log(x); 
    }

    valueAssignWithConst1();
    valueAssignWithConst2();
</script>
```

**输出:**

```
SyntaxError: Identifier 'x' has already been declared
```

**示例 3:** 在本例中，我们将看到使用**常量**对块范围进行操作

## 超文本标记语言

```
<script>
    function valueAssign() {
        const x = 10;
        var z = 15;
        if (true) {
            const y = 5;
            console.log(y); // Here y is 5
            console.log(x); // Here x is 10
            console.log(z); // Here z is 15
        }
        console.log(x); // Here x is 10
        console.log(z); // Here z is 15
        console.log(y); // Error: y is not defined  
    }

    valueAssign();
</script>
```

**输出:**

```
5
10
15
10
15
ReferenceError: y is not defined
```