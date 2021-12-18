# ES6 |进出口

> 原文:[https://www.geeksforgeeks.org/es6-import-and-export/](https://www.geeksforgeeks.org/es6-import-and-export/)

**ES6** 是一个 JavaScript 标准。在 ES6 的帮助下，我们可以用 JavaScript 创建模块。在一个模块中，可以有类、函数、变量和对象。要使所有这些在另一个文件中可用，我们可以使用**导出**和**导入**。**导出**和**导入**是用于导出和导入模块中一个或多个成员的关键字。

**导出:**您可以使用变量声明前面的**导出**关键字导出变量。您也可以通过执行相同的操作来导出函数和类。

*   **变量语法:**

    ```
    export let variable_name;
    ```

*   **函数语法:**

    ```
    export function function_name() {
      // Statements
    }

    ```

*   **类语法:**

    ```
    export class Class_Name {
      constructor() {
        // Statements
      }
    }

    ```

*   **示例 1:** 创建一个名为 **export.js** 的文件，并在该文件中编写下面的代码。

    ```
    export let num_set = [1, 2, 3, 4, 5];

    export default function hello() {
        console.log("Hello World!");
    }

    export class Greeting {
        constructor(name) {
            this.greeting = "Hello, " + name;
        }
    }
    ```

*   **Example 2:** In this example, we export by specifying the members of the module at the end of the file. We can also use alias while exporting using the **as** keyword.

    ```
    let num_set = [1, 2, 3, 4, 5];

    export default function hello() {
        console.log("Hello World!");
    }

    class Greeting {
        constructor(name) {
            this.greeting = "Hello, " + name;
        }
    }

    export { num_set, Greeting as Greet };
    ```

    **注意:**这里应该指定一个默认导出。

**导入:**可以使用**导入**关键字导入变量。您可以指定要从 JavaScript 文件导入的所有成员之一。

*   **语法:**

    ```
    import member_to_import from “path_to_js_file”;
    ```

    ```
    // You can also use an alias while importing a member.
    import Greeting as Greet from "./export.js";
    ```

    ```
    // If you want to import all the members but don’t
    // want to Specify them all then you can do that using
    // a ' * ' star symbol.
    import * as exp from "./export.js";
    ```

*   **示例 1:** 创建一个名为**import.html**的文件，并在该文件中编写以下代码。

    ```
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <title>Import in ES6</title>
        </head>
        <body>
            <script type="module">

                // Default member first
                import hello, { num_set, Greeting } from "./export.js";
                console.log(num_set);
                hello();
                let g = new Greeting("Aakash");
                console.log(g.greeting);
            </script>
        </body>
    </html>
    ```

*   **例 2:**

    ```
    <!DOCTYPE html>
    <html lang="en">
        <head>
            <title>Import in ES6</title>
        </head>
        <body>
            <script type="module">
                import * as exp from "./export.js";

                // Use dot notation to access members
                console.log(exp.num_set);
                exp.hello();
                let g = new exp.Greeting("Aakash");
                console.log(g.greeting);
            </script>
        </body>
    </html>
    ```

*   **输出:**输出将相同，导入相同的文件。
    T3】

**注意:**应该先导入默认成员，然后导入花括号中的 none 默认成员。