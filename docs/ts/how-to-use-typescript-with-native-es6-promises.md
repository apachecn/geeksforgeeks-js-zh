# 如何在原生 ES6 Promises 中使用 Typescript？

> 原文:[https://www . geesforgeks . org/how-using-typescript-with-native-es6-promises/](https://www.geeksforgeeks.org/how-to-use-typescript-with-native-es6-promises/)

**什么是打字稿？**
[TypeScript](https://www.geeksforgeeks.org/hello-world-in-typescript-language/) 是微软开发并维护的一种免费开源编程语言。它为 JavaScript IDEs 以及静态检查等实践提供了高效的开发工具。它甚至使代码更容易阅读和理解。我们可以使用 TypeScript 对普通的 JavaScript 进行巨大的改进。

**ES6 和 TypeScript:** [ES6](https://www.geeksforgeeks.org/introduction-to-es6/) 是 ECMAScript (ES)的一个版本，是由 ECMA 国际标准化的脚本语言规范。TypeScript 为我们提供了 ES6 的所有优势，并提高了工作效率。TypeScript 支持具有本机 ES6 生成器的机器的异步函数。通过这种方式，TypeScript 允许使用来自原生 ES6 的承诺。

**我们可以通过以下方式将 TypeScript 用于原生 ES6 承诺:**

1.  第一种方法是在 tsconfig.json 文件中添加以下代码行，如下所示:

```
"compilerOptions": {
    "lib": ["es5", "es2015.promise"]
}

```

这将包括原生 ES6 承诺的兼容性，而无需将目标设置为 ES6。

*   Another way to do the same is to add the following lines of code in the tsconfig.json file as shown below:

    ```
    "compilerOptions": {
        "target": "ES6"
    }

    ```

    使用上面的代码时，Promise 肯定应该存在于运行时中。

    *   There is also one more effective way to use Typescript with native ES6 promises. The following steps include:
    *   **第一步:**用 **{ }** 创建**包. json** 文件。
    *   **步骤 2:** 呼叫 **npm 安装–保存@ type/es6-承诺**。这将改变 package.json，以包含 ES6-promise 作为依赖项。
    *   **步骤 3:** 然后，调用**TSC–init**。这个命令为我们创建了 tfconfig.json 文件。
    *   **第四步:**现在，我们可以使用 **var x: Promise 在打字稿文件中使用 Promise；**
    *   **第五步:**执行 **tsc -p** 编译你创建的项目或程序。

    所有上述方法倾向于在所有浏览器中工作。通过这些，我们可以将 TypeScript 与本机 ES6 承诺结合使用。

    **演示承诺在异步/等待的类型脚本中使用的示例。**

    让我们看看承诺是如何在 TypeScript 函数中使用的。为此，下面创建了一个简单的承诺。这里，承诺被称为具有字符串的泛型类型，并且基本上执行两个操作，解析或拒绝。

    ```
    const val = new Promise((resolve, reject) => {});
    ```

    我们的承诺可以被解决或拒绝，这是通过以下代码来实现的，这就是所谓的回调。

    ```
    val.then(value => {
      console.log('resolved', value);
    });

    val.catch(error => {
      console.log('rejected', error);
    });
    ```

    给你。然后部分执行解析执行。catch 负责拒绝部分。如果承诺被解决，那么回调被执行。否则，将执行 catch 回调。

    要解决承诺，请使用以下代码:

    ```
    resolve("Hello");
    ```

    **输出:**

    ```
     resolved 'Hello'
    ```

    只有在特殊情况下才能拒绝承诺。不建议使用原始字符串拒绝承诺。相反，在拒绝承诺时，最好使用错误构造函数。

    拒绝承诺是通过以下代码完成的:

    ```
    reject(new Error('failed'));
    ```

    **输出:**

    ```
    rejected 'failed'
    ```

    像这样，ES6 承诺与 TypeScript 一起使用，仅仅通过使用 resolve/reject 就使回调的执行变得更容易和更快。