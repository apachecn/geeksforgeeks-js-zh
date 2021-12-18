# TypeScript | toString()函数

> 原文:[https://www.geeksforgeeks.org/typescript-tostring-function/](https://www.geeksforgeeks.org/typescript-tostring-function/)

TypeScript 中的 **toString()** 方法用于返回表示指定对象基数(base)的字符串。

**语法:**

```
number.toString( [radix] )
```

**参数:**该函数接受如上所述的单一参数，如下所述:

*   **radix:** This parameter represents an integer between 2 and 36 specifying the base to use for representing numeric values.

    **返回值:**返回表示指定数字对象的字符串。

    以下示例说明了 TypeScript 中的 **toString()函数**

    **例 1:**

    ## java 描述语言

    ```
    // The toString()function
    let Num1: number = 123;
    Num1.toString(); 
    Num1.toString(16); 
    Num1.toString(8); 
    Num1.toString(4);
    ```

    **输出:**

    ```
    123 
    7b
    173
    1323

    ```

    **例 2:**

    ## java 描述语言

    ```
    // The toString() function
    let Num2: number = 12345;   
    console.log("Number Method: toString()");  
    console.log(Num2.toString());  
    console.log(Num2.toString(4));
    ```

    **输出:**

    ```
    Number Method: toString()
    12345
    3000321

    ```