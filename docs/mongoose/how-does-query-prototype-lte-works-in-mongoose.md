# query . prototype . LTE()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-LTE-works-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-lte-works-in-mongoose/)

**Query.prototype.lte()** 函数用于指定$lte 查询条件。它返回小于或等于指定条件的文档。

**语法:**

```
Query.prototype.lte()
```

**参数:**该功能有*值*参数和可选路径参数。
**返回值:**此函数返回查询对象。

**猫鼬安装:**

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

var query = User.find()

query.where('age').lte(5).exec(function(err, res){
    if(err) console.log(err.message)
    else console.log(res)
});
```

项目结构会是这样的:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

> [ { _id: 5ebc367da99bde77b2efb9bf，姓名:‘piyus’，年龄:5，__v: 0 } ]

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

var query = User.find()

query.where('age').lte(25).exec(function(err, res){
    if(err) console.log(err.message)
    else console.log(res)
});

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

> 在 PORT 3000 上侦听的服务器
> [
> { _ id:5ebb 9129 a 99 bde 77 B2 efb 809，名称:' Gourav '，年龄:10，__v: 0 }，
> { _ id:5ebc 3669 a 99 bde 77 B2 efb 9 ba，名称:' Lalit '，年龄:25，__v: 0 }，
> { _ id:5ebc 367 da 99 bde 77 B2 efb 9 BF，名称:' Piyush '，

**参考:**T2https://mongoosejs.com/docs/api/query.html#query_Query-lte