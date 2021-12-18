# 如何在 JavaScript 中将字符串作为文字和对象进行测试？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中测试字符串作为文字和对象/](https://www.geeksforgeeks.org/how-to-test-a-string-as-a-literal-and-as-an-object-in-javascript/)

在本文中，我们学习如何使用 [JavaScript 将字符串作为文字和对象进行测试。](https://www.geeksforgeeks.org/javascript-tutorial/)

**什么是 JavaScript Literal？**

文字是在源代码中表示固定值的方式。在大多数编程语言中，值由整数、浮点数、字符串来标记，通常由布尔值和字符来标记，枚举类型和复合值(如数组、记录和对象)也由其他名称来标记。

**什么是 JavaScript 对象？**

每个对象都包含一个无序列表[<>](https://www.geeksforgeeks.org/html-ul-tag/)的原始数据类型(有时是引用数据类型)存储成对的名称和值。在列表中，每个项目都是一个属性。

***类型的*** **运算符:**JavaScript 中*类型的*运算符返回一个字符串，该字符串标识表达式的数据类型。它用于确定其操作数的数据类型(返回一个字符串)。操作数可以是文字或数据结构，如变量、函数或对象。运算符返回数据的类型。的*类型的结果可以是一个*对象*，一个*布尔*，一个*函数*，一个*数字*，一个*字符串*，或者一个*未定义的*值。*

**instanceof operator:** 检查 LHS(左侧)对象是否是 RHS(右侧)类的对象。如果对象属于该特定类别，则返回*真*否则返回*假*。

**示例:**在本例中，我们将使用 [if-else](https://www.geeksforgeeks.org/if-else-statement-in-javascript/) 条件来检查字符串是对象还是文字。

## 

```
<script>
    function check(str) {
        if(str instanceof String) {
            return "It is an object of string";
        } else {
            if(typeof str === "string") {
                return "It is a string literal";
            } else {
                return "another type";
            }
        }
    }

    // Pass a literal
    console.log(check("Hello geeks"));

    // Pass an object of string
    let s = new String("Hi");
    console.log(check(s));
</script>
```

**输出:**

```
It is a string literal
It is an object of string
```