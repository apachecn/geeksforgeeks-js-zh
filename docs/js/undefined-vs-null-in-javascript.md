# JavaScript 中未定义 Vs 为空

> 原文:[https://www . geesforgeks . org/undefined-vs-null-in-JavaScript/](https://www.geeksforgeeks.org/undefined-vs-null-in-javascript/)

null 和 undefined 之间有几个区别，它们有时被理解为相同的。

1.  **定义:**

    *   **Null:** 是该值的有意缺失。它是 JavaScript 的基本值之一。

    *   **Undefined:** 表示编译器中不存在该值。它是全局对象。

2.  **类型:**

    **空：** 对象

    **未定义:**未定义

3.  可以看参考[= =“vs”= = =“](https://www.geeksforgeeks.org/javascript-vs-comparision-operator/)篇。

    ```

     null == undefined // true
     null === undefined // false

    ```

    意思是*空*等于*未定义*但不相同。

4.  当我们将一个变量定义为*未定义*时，我们试图传达该变量不存在。
    当我们将一个变量定义为 *null* 时，我们试图传达这个变量是空的。

5.  **区分使用 isNaN():**
    大家可以参考 [NaN](https://www.geeksforgeeks.org/number-isnan-javascript/) 一文进行更好的
    理解。

    ```
    isNaN(2 +  null)      // false
    isNaN(2 + undefined) // true

    ```

6.  **示例:**

    *   **空：**

        ```
        null ? console.log("true") : console.log("false") // false

        ```

        *空*也称为*假*。

    *   **未定义:**

        当变量没有赋值时

        ```
        var temp;
        if(temp === undefined)
        console.log("true");
        else
        console.log("false");

        ```

        **输出:**

        ```
         true
        ```

        访问不存在的值

        ```
        var temp=['a','b','c'];
        if(temp[3] === undefined)
        console.log("true");
        else
        console.log("false");

        ```

        **输出:**

        ```
        true
        ```