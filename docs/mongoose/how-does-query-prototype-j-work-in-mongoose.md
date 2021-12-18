# query . prototype . j()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-j-work-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-j-work-in-mongoose/)

**Query.prototype.j()** 函数用于请求确认此操作已被保存到 MongoDB 的磁盘日志中。

**语法:**

```
Query.prototype.j()
```

**参数:**该函数有一个布尔类型的值参数。
**返回值:**该函数返回查询对象。
安装獴:

```
npm install mongoose
```

安装猫鼬模块后，可以使用命令在命令提示符下检查您的**猫鼬**版本。

```
npm mongoose --version
```

之后，您可以创建一个文件夹并添加一个文件，例如 index.js，如下所示。

**数据库:**这里使用的样本数据库如下所示:

![](img/2134265eb70c448baf37786789f2598a.png)

**示例 1:**
**文件名:index.js**

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

const query = User.updateOne({name:"Gourav"}, { $set: {name: 'Geek'} }).j(true);
console.log("Above operation has been persisted to MongoDB's on-disk journal")
```

项目结构会是这样的:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Above operation has been persisted to MongoDB's on-disk journal
```

**示例 2:**
**文件名:index.js**

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

const query = User.updateOne({name:"Gourav"}, { $set: {name: 'Geek'} }).j(false);
console.log("Above operation has not been persisted to MongoDB's on-disk journal")

app.listen(3000, function(error ) {
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
});
```

项目结构会是这样的:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Server listening on PORT 3000
Above operation has not been persisted to MongoDB's on-disk journal
```

**参考:**T2[https://mongoosejs.com/docs/api/query.html#query_Query-j](https://mongoosejs.com/docs/api/query.html#query_Query-j)T5】