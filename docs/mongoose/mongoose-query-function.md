# 猫鼬查询()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-query-function/](https://www.geeksforgeeks.org/mongoose-query-function/)

查询构造函数用于构建查询。因此用户不需要直接实例化查询。“查询”是“查询”的一个实例。

**语法:**

```
Query()

```

**参数:**该功能有可选参数，如模型、条件、集合和选项。

**返回值:**该函数返回查询对象。

**猫鼬模块安装:**

*   可以访问[安装猫鼬模块](https://www.npmjs.com/package/mongoose)的链接。您可以使用此命令安装此软件包。

```
npm install mongoose

```

*   安装猫鼬模块后，可以使用命令在命令提示符下检查您的**猫鼬**版本。

```
npm version mongoose

```

*   之后，您可以创建一个文件夹并添加一个文件，例如 index.js，如下所示。

**示例 1:** **文件名:index.js**

## java 描述语言

```
const express = require('express');
const mongoose = require('mongoose');
const app = express()

// Database connection
mongoose.connect('mongodb://127.0.0.1:27017/geeksforgeeks', {
    useNewUrlParser: true,
    useCreateIndex: true,
    useUnifiedTopology: true
});

// User model
const User = mongoose.model('User', { 
    name: { type: String },
    age: { type: Number }
});

const query = new mongoose.Query();
console.log(query);

app.listen(3000, function(error ){
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
})
```

**运行程序的步骤:**

*   项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

*   使用以下命令运行 **index.js** 文件:

```
node index.js

```

**输出:**

```
Query {
  _mongooseOptions: {},
  _transforms: [],
  _hooks: Kareem { _pres: Map {}, _posts: Map {} },
  _executionCount: 0,
  op: undefined,
  options: {},
  _conditions: {},
  _fields: undefined,
  _update: undefined,
  _path: undefined,
  _distinct: undefined,
  _collection: undefined,
  _traceFunction: undefined,
  '$useProjection': true
}
Server listening on PORT 3000

```

**示例 2:** **文件名:index.js**

## java 描述语言

```
const mongoose = require('mongoose');

// Database connection
mongoose.connect('mongodb://127.0.0.1:27017/geeksforgeeks', {
    useNewUrlParser: true,
    useCreateIndex: true,
    useUnifiedTopology: true
});

// User model
const User = mongoose.model('User', { 
    name: { type: String },
    age: { type: Number }
});

const query = new mongoose.Query();
query.collection(User.collection);
console.log(query);
```

**运行程序的步骤:**

*   项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

*   使用以下命令运行 **index.js** 文件:

```
node index.js

```

**输出:**

```
Query {
  _mongooseOptions: {},
  _transforms: [],
  _hooks: Kareem { _pres: Map {}, _posts: Map {} },
  _executionCount: 0,
  op: undefined,
  options: {},
  _conditions: {},
  _fields: undefined,
  _update: undefined,
  _path: undefined,
  _distinct: undefined,
  _collection: NodeCollection {
    collection: NativeCollection {
      collection: null,
      Promise: [Function: Promise],
      _closed: false,
      opts: [Object],
      name: 'users',
      collectionName: 'users',
      conn: [NativeConnection],
      queue: [],
      buffer: true,
      emitter: [EventEmitter]
    },
    collectionName: 'users'
  },
  _traceFunction: undefined,
  '$useProjection': true
}

```

**参考:**T2https://mongoosejs.com/docs/api/query.html