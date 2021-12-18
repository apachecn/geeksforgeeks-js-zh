# 如何添加第三方库 Deno.js？

> 原文:[https://www . geesforgeks . org/how-add-第三方-library-deno-js/](https://www.geeksforgeeks.org/how-to-add-third-party-library-deno-js/)

今天我们将学习如何将自己的模块添加到 [deno.js](https://www.geeksforgeeks.org/deno-js-introduction/) 中，供用户使用。我们知道，在任何语言或环境中都添加了标准模块。类似地，在 Deno.js 中，许多内置/标准模块可供用户使用。

向语言或环境中添加一个新模块可以在很多方面帮助一个人——一个人学习如何为开源做贡献，以及如何编写测试过的模块和脚本，以便用户能够以最好的方式使用它们。

**先决条件:**

1.  熟悉 JavaScript 或 TypeScript
2.  在机器上安装 Deno.js。(在命令行中输入 **deno -v** 确认)。
3.  熟悉 GitHub 以及如何拉、叉一个资源库。

**代码结构:**要开始使用向 Deno.js 添加模块的代码结构，需要遵循特定的文件结构。

```
git clone https://github.com/guptamohit004/ip_details
cd ip_details

```

这是我添加的模块之一。需要遵循相同的模式将模块添加到 DENO 中。

因此，让我们看看代码结构，了解您需要做什么。

*   **mod . ts–**通常是任何模块的入口点。需要在这个文件中编写主要的函数/代码。它类似于 Node.js 中的 index.js/app.js
*   **CLI . ts–**当使用 CLI 中的模块时，该文件将被执行。在这里，您可以定义在执行脚本时需要传递哪些参数。
*   **MOD_TEST。TS–**它是在开发过程中使用的文件，用于从 CLI 测试模块。在这个标准库中，Deno 用于获取 Deno 中的测试功能。
*   **自述。MD–**该文件为查看者/用户提供了与模块相关的所有信息，如如何使用模块、将会有什么请求和什么响应，以及如何在不同情况下使用模块，如 CLI、从模块导入、bash 等。需要添加这个[图像](https://github.com/denorg/get-ip/workflows/Test%20CI/badge.svg)来测试所有的案例，以便从 Deno 网站获得该模块。
    **重要提示–**您需要添加此文件中的所有配置/权限，例如–允许网络、–允许读取、–允许写入。

**PACKAGE 在哪里。JSON？**我们知道，在使用 Node.js 开发模块时，我们需要在代码文件夹中有一个 Package.json 文件。但是在使用 Deno 的情况下，不需要有这样的文件，可以直接使用网址中的模块，并将其存储在计算机缓存中。

现在开始构建您的模块，并从命令行界面以及使用测试命令运行和测试它。

现在是出版部分--

1.  将您的模块添加到您的 Github 中，并从您的 repo 中启用操作。
2.  公开回购协议。
3.  现在转到 [DATABASE.JSON.](https://github.com/denoland/deno_website2/blob/master/database.json)
4.  按照以下格式添加您的模块详细信息。

    ```
    "my_library_name": {
        "type": "github",
        "owner": "",
        "repo": "<my_repository_name>"
    }</my_repository_name>
    ```

5.  现在创建拉请求来更新文件。
6.  在 Deno 上写下“添加‘您的模块名称’。
7.  发出拉取请求。
8.  现在你的更新文件需要通过一些测试，你可以走了。
9.  已成功创建请求。等待批准。