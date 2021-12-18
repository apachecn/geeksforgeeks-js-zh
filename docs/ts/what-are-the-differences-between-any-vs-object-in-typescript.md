# TypeScript 中任意 vs 对象有什么区别？

> 原文:[https://www . geesforgeks . org/any-vs-object-in-typescript/](https://www.geeksforgeeks.org/what-are-the-differences-between-any-vs-object-in-typescript/)有什么区别

**[TypeScript](https://www.geeksforgeeks.org/hello-world-in-typescript-language/)** 是一种开源编程语言。它是 JavaScript 语言的超集。TypeScript 是为开发大型应用程序而设计的。

**any:** 它是 TypeScript 中的内置数据类型，有助于描述我们在编写代码时不确定的变量类型。
虽然数据类型‘any’很有用，但不应该不必要地使用。

*   **语法:**

    ```
    var x: any; // This means x has no interface.

    ```

*   **特征:**
    *   当没有可用的类型定义时，可以使用此数据类型。
    *   “任何”数据类型可以用来表示任何 JavaScript 值。
*   **示例:**以下代码说明了类型脚本中的任何数据类型:
    *   **代码 1:**

        ```
        <script>
        function add(one: any, two: any): number {
          return one + two;
        }

        console.log(add('Geeks', 'forgeeks'));     

        </script>                    
        ```

    *   **输出:**

        ```
        Geeksforgeeks
        ```

    *   **代码 2:**

        ```
        <script>
        function subtract(one: any, two: any): number {
          return one - two;
        }

        console.log(subtract(9, 5)); 
        </script>
        ```

    *   **输出:**

        ```
        4
        ```

**Object:** 它描述了功能，Object 有助于表示除了数字、字符串、布尔、大 int、符号、undefined 和 null 之外的所有非基元类型。在类型脚本中，对象(高位)不同于对象(低位)。

*   **语法:**

    ```
    var y: Object; // This means y has Object interface.

    ```

*   **特征:**
    *   对象公开了在对象类中定义的函数和属性。
    *   对象是一种更具体的声明方式。
*   **示例:**以下代码说明了类型脚本中的对象:
    *   **代码 1:**

        ```
        <script>  
            Student={roll_no:11,name:"XYZ"}  
            document.write(Student.roll_no+" "+Student.name+" ");  
        </script>
        ```

    *   **输出:**

        ```
        11 XYZ
        ```

    *   **代码 2:**

        ```
        <script>  
            emp={id:102,name:"ABC",salary:10000}  
            document.write(emp.id+" "+emp.name+" "+emp.salary);  
        </script> 
        ```

    *   **输出:**

        ```
        102 ABC 10000
        ```

**类型脚本中任意和对象的区别:**

| 任何的 | 目标 |
| --- | --- |
| 如果您对 nomethod()函数使用“any ”,那么您基本上是在告诉 transpiler，不会提供关于存储在其中的信息。因此，transpiler 不限制任何东西，并且它传输得很好。 | Object 类没有 nomethod()函数，因此 transpiler 会产生一个错误计算。 |
| 使用起来比对象更灵活。 | 对象在声明中比任何。 |
| 任何不忽略任何编译时检查。 | 对象需要更多的时间来编译。 |