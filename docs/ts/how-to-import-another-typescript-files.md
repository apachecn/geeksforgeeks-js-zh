# 如何导入另一个类型脚本文件？

> 原文:[https://www . geesforgeks . org/如何导入另一个类型脚本文件/](https://www.geeksforgeeks.org/how-to-import-another-typescript-files/)

有些时候，我们想要一些我们在以前的项目中使用过的工具，在这种情况下，我们不能再次重写那个脚本，我们可以简单地通过导出那个文件来导入它。要将其他类型脚本文件导入到现有的类型脚本文件中，我们应该知道**模块**的概念。从 **ECMAScript 2015** 开始，JavaScript 就有了模块的概念，TypeScript 也有这个概念。

模块是独立的、可重用的代码的小单元，希望用作构建模块。模块允许开发人员分别定义私有和公共成员，使其成为脚本范例中更理想的设计模式之一。您可以像在任何其他面向对象编程语言中一样，将模块视为类。从不同模块导出，必须使用其中一个**导入**表单导入。

**示例 1:** 将一个类从一个文件导入到另一个文件。

*   **Code 1:** This code file will be imported, and the file name will be saved as **exportedFile.ts** in the directory.

    ```
    // Exporting the class which will be
    // used in another file
    // Export keyword or form should be
    // used to use the class 
    export class exportedFile {

        // Class method which prints the
        // user called in another file
        sayHello(user){
            return "Hello " + user+ "!";
        }
    }
    ```

*   **Code 2:** This code file will import the above code and save the file as the name **mainFile.ts** in the same directory.

    ```
    // Importing the class from the location of the file
    import { exportedFile } from "./exportedFile";

    // Creating an object of the class which is imported
    let user = new exportedFile();

    // Calling the imported class function
    console.log(user.sayHello("Geek"));
    ```

*   **Output:**

    ```
    Hello Geek!
    ```

**注意:**你要编译 **mainFile.ts** 生成 **mainFile.js** 运行 js 文件。

在要导入的 TypeScript 文件中必须包含一个**导出**表单，导入类的主文件必须包含一个**导入**表单，通过该表单 TypeScript 可以识别所使用的文件。通过使用这种类型的**导出**和**导入**表单，我们可以导入**类、接口、函数、变量**任何我们想要的东西。

**示例 2:** 我们也可以根据需要通过重命名来导入它们。通过重命名函数从另一个文件导入函数。

*   **Code 1:** Save this file as **exported file.ts**

    ```
    // Exporting the function which will be
    // used in another file
    export function sayHello(user:string) {
        return "Hello " + user + "!";
    }
    ```

*   **Code 2:** Save this file as **main file. ts**

    ```
    // Importing the function sayHello and renaming it 
    // from the location of the file
    import { sayHello as hello } from "./exportedFile";

    let user = "Jake";

    // Calling the imported function
    console.log(hello(user));
    ```

*   **Output:**

    ```
    Hello Jake!
    ```

**示例 3:** 我们可以使用如下所示的导入所有表单来导入文件的所有内容。全部导入表示为**“导入*”**。

*   **Code 1:** Save this file as **exported file.ts**

    ```
    // Here we have to export all the
    // class, interface, function 
    export class sayGoodByeTo {
        goodbye(user: string) {
            return "Good bye " + user + "!";
        }
    }
    export interface howareYou {
        howareyou(user: string) : string;
    }
    export function sayHello(user:string) {
        return "Hello " + user + "!";
    }
    ```

*   **Code 2:** Save this file as **main file. ts**

    ```
    // Importing everything from the exportedFile.ts module
    // Import all is indicated using 'import *' 
    // and here 'as' keyword 
    import * as importAll from "./exportedFile";
    let user = "Geeks";

    // Calling the imported function
    console.log(importAll.sayHello(user));

    // Implementing the imported interface
    class hru implements importAll.howareYou {
        howareyou(user: string){
            return "How are you "+user+"!";
        }
    }

    // Calling the implemented function in the 
    // Interface which is imported
    let jd = new hru();
    console.log(jd.howareyou(user));

    // Creating the object of the imported class
    // and calling it's function
    let bye = new importAll.sayGoodByeTo();
    console.log(bye.goodbye(user));
    ```

*   **Output:**

    ```
    Hello Geeks!
    How are you Geeks!
    Good bye Geeks!

    ```

**注意:**要全部导入，需要重命名模块。当我们使用**作为**关键字时，它基本上是将所有的类、函数、接口包装在一个模块中。我们也可以通过简单地编写多个导入表单和模块位置来导入多个文件。