# TypeScript 中私有关键字和私有字段的区别

> 原文:[https://www . geesforgeks . org/private-keyword 和-private-field-in-typescript 的区别/](https://www.geeksforgeeks.org/difference-between-private-keyword-and-private-fields-in-typescript/)

TypeScript 3.8 支持 **private 关键字**声明其成员为私有。TypeScript 中的**私有字段**是为 JavaScript 新提出的。这些字段前面是 **#** 。

**private 关键字:**TypeScript 中的 Private 关键字用于标记成员 Private，这使得它在声明的类之外不可访问。字段前面有 **private** 关键字来标记它们为 private。

*   **语法:**

    ```
    private variableName
    ```

*   **例:**

    ```
    class letters { 
        private a;

        constructor(alphabet){ 
            this.a = alphabet;
        } 

        getA(){
            return this.a;
        }
    } 
    const l = new letters("gfg"); 
    console.log(l.getA()); 
    ```

*   **输出:**

    ```
    gfg
    ```

**私有字段:**TypeScript 中的私有字段是新添加到 JavaScript 中的字段，要声明为私有的成员前面有一个 **#** 。私有成员不能在他们的类之外被访问。

*   **语法:**

    ```
    #variableName
    ```

*   **Example:**

    ```
    class letters {
        #a;

        constructor(alphabet){
            this.#a = alphabet;
        }

        getA(){
            return this.#a;
        }
    }
    const l = new letters("gfg");
    console.log(l.getA());            
    ```

    **输出:**

*   ```
    gfg
    ```

因此，要在运行时将 TypeScript 编译为 ESNext JavaScript 时实现私有关键字，必须考虑使用为 JavaScript 定义的私有语法 **#** 。

**私有关键字和私有字段的区别:**

| 私有关键字 | 私有字段 |
| --- | --- |
| 它是一个 TypeScript 修饰符。 | 这是 ECMA 新添加到 JavaScript 中的语法，也可以在 TypeScript 中找到。 |
| 这是一个编译时注释。所以，当 transpiler 将 TypeScript 代码转换为 JavaScript 时，私有关键字**被移除**。 | 私有字段在运行时保持私有，即使 TypeScript 代码被 transpiler 转换为 JavaScript。 |