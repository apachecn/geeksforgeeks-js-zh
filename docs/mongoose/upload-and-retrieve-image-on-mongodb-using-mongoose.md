# 使用猫鼬在 MongoDB 上上传和检索图像

> 原文:[https://www . geeksforgeeks . org/上传和检索图像-on-MongoDB-using-mongose/](https://www.geeksforgeeks.org/upload-and-retrieve-image-on-mongodb-using-mongoose/)

**先决条件:**要开始使用这个，您应该对 **NodeJS** 、 **ExpressJS** 、 **MongoDB** 和**mongose**有所了解。

*   [**NodeJS**](https://www.geeksforgeeks.org/introduction-to-nodejs/) **:** 是一个在服务器上使用 JavaScript，运行在各种平台(Windows、Linux、Unix、Mac OS X 等)上的免费开源服务器环境。).它使用异步编程。
*   [**ExpressJS**](https://www.geeksforgeeks.org/introduction-to-express/)**:**是 NodeJS web 应用服务器框架，设计用于构建单页、多页和混合 web 应用。它是节点事实上的标准服务器框架。
*   [**MongoDB**](https://en.wikipedia.org/wiki/MongoDB)T4:MongoDB 是一个 NoSQL 数据库。MongoDB 是一个 JSON 文档数据存储库。它允许您存储和查询 JSON 风格的文档，上面有一些智能。
*   [**【猫鼬】**](https://mongoosejs.com/) **:** 猫鼬是一个针对 MongoDB 和 Node 的对象数据建模(ODM)库。js。它管理数据之间的关系，提供模式验证，并用于在代码中的对象和 MongoDB 中这些对象的表示之间进行转换。

首先，安装所需的软件包和模块:

*   ExpressJS 允许我们设置中间件来响应 HTTP 请求。

```
npm install express --save
```

*   模块“正文解析器”支持读取(解析)HTTP-POST 数据。

```
npm install body-parser --save
```

*   Mongoose 是一个 MongoDB 客户端库，提供用于异步环境的对象建模。猫鼬支持承诺和回调。

```
npm install mongoose --save
```

*   Multer 是用于上传文件的 **nodejs** 中间件。

```
npm install multer --save
```

*   Dotenv 是一个零依赖模块，它将环境变量从. env 文件加载到 process.env 中。

```
npm install dotenv --save
```

*   EJS ( *嵌入式 Javascript* )是 **nodejs** 的模板引擎。这个引擎有助于通过模板用最少的代码创建一个网页。

```
npm install ejs --save
```

*   nodemon 是一个开发工具，当检测到代码目录中的文件更改时，它会自动重新启动节点应用程序。它改善了开发人员在处理基于节点的应用程序时的体验。因为这是一个开发工具，不是我们应用程序代码的一部分，所以我们在安装这个模块时使用`–save-dev `:

```
npm install nodemon --save-dev
```

现在让我们开始编码吧！要使用**芒果**上传图像并通过**蒙古数据库**检索图像，请逐一执行以下步骤。

*   **第 0 步:**创建文件` ***。env*** `将包含特定于环境的设置。

## java 描述语言

```
MONGO_URL=mongodb://localhost/imagesInMongoApp
PORT=3000
```

*   **第一步:**创建我们的服务器文件` ***app.js*** **`** 。向其中添加以下代码:

## java 描述语言

```
// Step 1 - set up express & mongoose

var express = require('express')
var app = express()
var bodyParser = require('body-parser');
var mongoose = require('mongoose')

var fs = require('fs');
var path = require('path');
require('dotenv/config');
```