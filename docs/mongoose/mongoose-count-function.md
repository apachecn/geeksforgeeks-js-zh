# 猫鼬计数()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-count-function/](https://www.geeksforgeeks.org/mongoose-count-function/)

**Query.prototype.count()** 函数用于统计集合中的文档数量。这个函数基本上将这个查询指定为计数查询。

**语法:**

```
Query.prototype.count()

```

**参数:**此函数接受一个数组参数，即回调函数。

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

**数据库:**这里使用的样本数据库如下所示:

![](img/2134265eb70c448baf37786789f2598a.png)

**示例 1:** **文件名:index.js**

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

var query = User.find();
query.count(function (err, count) {
    if (err) console.log(err)
    else console.log("Count is", count)
});
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
Count is 4

```

**示例 2:** **文件名:index.js**

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

var query = User.find();
query.count(function (err, count) {
    if (err) console.log(err)
    else console.log("Count:", count)
});

app.listen(3000, function(error ) {
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
});
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
Server listening on PORT 3000
Count: 4

```

**参考:**[https://mongoosejs . com/docs/API/Query . html # Query _ Query-count](https://mongoosejs.com/docs/api/query.html#query_Query-count)