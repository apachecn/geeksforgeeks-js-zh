# query . prototype . batchsize()在 Mongoose 中是如何工作的？

> 原文:[https://www . geeksforgeeks . org/how-do-query-prototype-batch size-work-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-batchsize-work-in-mongoose/)

**query . prototype . batchSize()**用于设置 batchSize 选项。batchSize()函数基本上指示驱动程序每次检索一定数量的项目。
**语法:**

```
Query.prototype.batchSize()
```

**参数:**该函数有一个数组参数，即定义批次大小的数字。
**返回值:**该函数返回查询对象。

安装猫鼬:

```
npm install mongoose
```

安装猫鼬模块后，可以使用命令在命令提示符下检查您的**猫鼬**版本。

```
npm mongoose --version
```

之后，您可以创建一个文件夹并添加一个文件，例如 index.js，如下所示。

**例 1:**

## index.js

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

const query = User.find(); 
query.batchSize(100);

console.log("The batch size set is :", query.options)
```

项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
The batch size set is : { batchSize: 100 }
```

**例 2:**

## index.js

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

const query = User.find(); 
query.batchSize(140);

console.log("Batch Size defined is:", query.options)

app.listen(3000, function(error ){
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
})
```

项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Server listening on PORT 3000
Batch Size defined is: 140
```

**参考:**[https://mongoosejs . com/docs/API/Query . html # Query _ Query-batchSize](https://mongoosejs.com/docs/api/query.html#query_Query-batchSize)