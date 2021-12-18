# JavaScript 中静态和常量的区别

> 原文:[https://www . geesforgeks . org/static 和 const-in-javascript 的区别/](https://www.geeksforgeeks.org/difference-between-static-and-const-in-javascript/)

[**静态变量**](https://www.geeksforgeeks.org/how-to-create-static-variables-in-javascript/)**:**JavaScript 中的静态变量基本上是类的一个属性，它不在类的对象上使用，而是在类本身中使用。这个静态变量存储在内存的数据段中，其值在该特定类中创建的所有对象/实例之间共享。为了将变量/函数声明为静态的，我们使用了“ *static* ”关键字。在静态变量的情况下，它的值是在运行时本身设置的，并且它是一个全局值，可以由类的实例使用。

**示例:**在下面的代码中，我们已经在 z 类中声明了一个静态方法，并使用 [**文档将其打印出来。**写()](https://www.geeksforgeeks.org/html-dom-write-method/)法。

## Java Script 语言

```
<script>  
    class z {  
        static staticMethod() {  
            return "Displaying geeks for "
              + "geeks using static method.";  
        }  
    }  
    document.write(z.staticMethod());  
</script>  
```

**输出:**

![](img/565dcc7b9c7ac9212b8940a9e622901e.png)

**常量:**JavaScript 中的常量变量是一个具有常量或固定值的变量，保持不变。这在整个程序中不会改变。一旦声明，就不可能对其值进行任何修改。如果程序员试图修改它的值，编译器会显示一个错误，这是因为一旦我们将一个变量声明为常量，它就会告诉编译器这是一个固定值，应该防止对其进行任何更改。

**示例:**下面是 [*const*](https://www.geeksforgeeks.org/javascript-const/) 关键字在 JavaScript 中的实现。在下面的代码中，我们已经将一个变量声明为 *const* ，并使用[**document . write()**](https://www.geeksforgeeks.org/html-dom-write-method/)方法显示了它的值。

## Java Script 语言

```
<script>  
    const value= 8; 
    document.write(value);  
</script>     
```

**输出:**

```
8
```

**Static 与 Constant 的区别:**

<figure class="table">

| **静态** | **恒定** |
| Static methods are basically utility functions for creating or making copies of objects. | The [T0】 const 【T1] variable is basically used to declare an unmodifiable constant value. |
| A *static* keyword is used to declare a variable or a method static. | A *constant* keyword is used to assign a constant or a fixed value to a variable. |
| In JavaScript, the static keyword is also used for methods and classes. | In JavaScript, the keyword *const* is also used for arrays and objects. |
| The values of static variables can be modified. | The value of a constant cannot be modified. |
| Static is a storage specifier. | Const/Const is a type qualifier. |
| Static can be assigned as a reference type and set at run time. | Constants themselves are set at compile time, and only value types are assigned values. |

</figure>