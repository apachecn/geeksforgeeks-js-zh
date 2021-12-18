# 解释 for(..in)和 for(..of)语句。

> 原文:[https://www . geeksforgeeks . org/解释 javascript 语句中的 for 和 for 之间的差异/](https://www.geeksforgeeks.org/explain-the-differences-between-for-in-and-for-of-statement-in-javascript/)

通常在一个 JavaScript 脚本中，我们迭代一些很少内置类的对象，比如数组、字典、字符串、映射等。我们使用循环迭代对象。JavaScript 支持不同类型的循环:

*   for 循环
*   用于(..in)循环
*   用于(..of)循环
*   while 循环
*   边做边循环

在本文中，我们将学习 for(..in)和 for(..的)循环。

**为(..in)循环:**用于(..in)语句循环遍历对象的可枚举属性。循环将遍历对象本身的所有可枚举属性以及对象从其构造函数原型继承的属性。

*   **语法**

    ```
    for (variable in object)
      statement
    ```

*   **例**T0】

*   **Output:** As you can see the for (..in) loop iterate over only the properties or the values of the dictionary object.

    ```
    GeeksforGeeks
    A Computer Science Portal for Geeks 43
    ```

    **为(..of)循环:**此为(..语句允许您循环访问可迭代的数据结构，如数组、字符串、映射、节点列表等。它调用带有指令的自定义迭代钩子，对对象的每个属性值执行。

    *   **语法**

        ```
        for (variable of iterable) {
          statement
        }

        ```

    *   **例**T0】
    *   **输出:**如您所见(..of)循环仅迭代数组对象的内容。

        ```
        GeeksforGeeks A Computer Science Portal for Geeks 43
        ```