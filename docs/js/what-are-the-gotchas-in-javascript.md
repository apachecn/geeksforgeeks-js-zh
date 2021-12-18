# JavaScript 中有哪些陷阱？

> 原文:[https://www . geeksforgeeks . org/什么是 javascript 中的陷阱/](https://www.geeksforgeeks.org/what-are-the-gotchas-in-javascript/)

Javascript 确实是一种流行的语言，因为它简单且多功能。尽管 Javascript 有很多优点，但它是一种有趣的语言，有时会让你感到困惑，尤其是对于那些习惯于传统面向对象语言的人来说。

*   **= = vs = = = =***   **区分大小写***   剖析*   **自动分号插入**
    *   **‘ == ‘ is not the same as ‘===’ :** Not all equality signs mean the same. The double equal operator follows type coercion which means that both the data types of the variable do not need to match.The triple equality operator is a strict equality operator i.e it will perform a type coercion.
        **Example:**

        ```
        console.log(12 == '12')
        console.log( 12 === '12')
        ```

        如果在控制台上运行，它会给出以下输出:

        ```
        true
        false
        ```

        这意味着，当我们使用“==”运算符时，它会将 12 的字符串转换为一个数字，并对这些数字进行比较。因为它们是相同的数字，所以它返回一个真值。在' === '运算符中，它遵循严格类型并检查数据类型和值。因为一个数据类型是字符串，另一个是数字类型，所以它返回一个假值。

    *   **Case sensitive :** Identifiers are used to name keywords, variables and functions.Like most programming languages, the rules for naming a variable are also the same. As javascript is case-sensitive,
        the first character of an identifier could be a letter or a dollar sign but it **cannot** be a number. Two variables need not be the same. **Example:**

        ```
        age ="20";
        Age = "23";

        ```

        这里，年龄和年龄是两个独立的字符串变量。

        **注意:Javascript 遵循 camel 大小写符号。**

    *   剖析:t1]
        *   第一个参数-获取要解析的字符串。*   第二个参数——数字的基数。范围可以从 2 到 36。

**语法:**

```
parseInt(string, radix)
```

在大多数情况下，默认基数是基数 10。但是，如果数字以 **0x** 开头，则假设字符串将被解析为**基数 16** ，如果数字以 **0** 开头，则假设基数为 **8** 。
**示例:**

```
parseInt("02", 10); 
parseInt("0x11"); 
```

**输出:**

```
 2
 17
```

*   **Automatic semi-colon insertion:** Although semi-colons are optional in Javascript it is a good practice to add them wherever needed. This is because javascript automatically adds semi-colon to your code and could throw an error. **Consider a classic example of ASI(Automatic semi-colon insertion):**

    ```
    function foo1()
    {  
    return {       
    bar: "hello"  
    };
    } 

    function foo2()            
    {  
    return   {     
     bar: "hello" 
     };
     }

    console.log("foo1 returns:");
    console.log(foo1());
    console.log("foo2 returns:");
    console.log(foo2());
    ```

    **输出:**

    ```
    foo1 returns:
     Object {bar: "hello" }
     foo2 returns:
     undefined
    ```

    首先在上面的代码中，看起来它们返回了同一个对象，但是第二个对象没有返回，并且由于 ASI 的原因返回了一个值 **undefined** 。