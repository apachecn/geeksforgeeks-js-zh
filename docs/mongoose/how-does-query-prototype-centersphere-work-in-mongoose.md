# query . prototype . center sphere()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-center sphere-in-work-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-centersphere-work-in-mongoose/)

函数的作用是:为使用球面几何的*地理空间*查询定义一个圆。它返回圆边界内的所有文档。

**语法:**

```
Query.prototype.centerSphere()
```

**参数:**该函数有一个值参数和一个可选的路径参数。
**返回值:**该函数返回查询对象。

安装猫鼬:

```
npm install mongoose
```

安装猫鼬模块后，可以使用命令在命令提示符下检查您的**猫鼬**版本。

```
npm mongoose --version
```

现在，创建一个文件夹并添加一个文件，例如 index.js，如下所示。

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

var query = User.find();
var area = { center: [20, 20], radius: 5, unique: true }
query.where('loc').within().centerSphere(area)

console.log(query._conditions.loc.$geoWithin)
```

1.  项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

```
node index.js
```

**输出**:

```
{ '$centerSphere': [ [ 20, 20 ], 5 ], '$uniqueDocs': true }
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

var query = User.find();
var area = { center: [10, 10], radius: 50, unique: true }
query.where('loc').within().centerSphere(area)

console.log(query._conditions.loc.$geoWithin)

app.listen(3000, function(error ) {
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
});
```

1.  项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

```
node index.js
```

**输出**:

```
Server listening on PORT 3000
{ '$centerSphere': [ [ 10, 10 ], 50 ], '$uniqueDocs': true }
```

**参考:**[https://mongoosejs . com/docs/API/Query . html # Query _ Query-center sphere](https://mongoosejs.com/docs/api/query.html#query_Query-centerSphere)