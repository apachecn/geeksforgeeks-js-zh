# JavaScript |管道操作符

> 原文:[https://www.geeksforgeeks.org/javascript-pipeline-operator/](https://www.geeksforgeeks.org/javascript-pipeline-operator/)

JavaScript 管道操作符 **( | > )** 用于将表达式的值输送到函数中。这个操作符使链式函数更易读。使用 **( | > )** 运算符调用该函数，管道运算符上使用的任何值都将作为参数传递给该函数。函数按照对参数进行操作的顺序排列。

**语法:**

```
expression |> function
```

**使用 Pipeline Operator:** 由于 Pipeline Operator 是一个实验性特性，目前处于第 1 阶段提案中，因此不支持当前可用的浏览器，因此也不包含在 Node 中。然而，人们可以使用巴贝尔(JavaScript 编译器)来使用它。

**步骤:**

*   在继续之前，请确保安装了 Node.js。
*   在桌面上创建一个目录(比如 pipeline-operator)，并在该目录中创建一个 JavaScript 文件(比如 main.js)。
*   导航到该目录并初始化一个 **package.json** 文件，该文件包含关于项目及其依赖项的相关信息。

    ```
    npm init

    ```

*   安装 babel 以便使用操作员。管道操作符目前不是 JavaScript 语言的一部分，巴贝尔用于编译代码，以便 Node 能够理解。

    ```
    npm install @babel/cli @babel/core 
        @babel/plugin-proposal-pipeline-operator 

    ```

*   为了指导 babel 正确编译代码，一个名为**的文件。巴别尔克**由以下线条创建:

    ```
    {
      "plugins": 
      [
          [
              "@ babel/plugin-proposal-pipeline-operator",
              {
                  "proposal" : "minimal"
              }    
          ]
      ]
    }

    ```

*   添加一个**开始**脚本到 package.json 文件，该文件将运行巴别塔:

    ```
    "start" : "babel main.js --out-file output.js && node output.js"

    ```

*   运行代码:

    ```
    npm start
    ```

**例:**

## Javascript

```
// JavaScript Code (main.js)

function add(x) {
    return x + 10;
}

function subtract(x) {
    return x - 5;
}

// Without pipeline operator
let val1 = add(subtract(add(subtract(10))));
console.log(val1);

// Using pipeline operator

// First 10 is passed as argument to subtract
// function then returned value is passed to
// add function then value we get is passed to
// subtract and then the value we get is again
// passed to add function
let val2 = 10 |> subtract |> add |> subtract |> add;
console.log(val2);
```

**输出:**

```
20
20
```