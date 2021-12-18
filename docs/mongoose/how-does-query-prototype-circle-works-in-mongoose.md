# query . prototype . circle()在猫鼬中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-circle-works-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-circle-works-in-mongoose/)

**Query.prototype.circle()** 函数用于指定$center 或$centerSphere 条件。它为$ GeoInTerface 查询指定了一个圆。
**语法:**

```
Query.prototype.circle()
```

**参数:**该功能有一个面积参数和一个可选路径参数。
**返回值:**该函数返回查询对象。

安装猫鼬:

```
npm install mongoose
```

安装猫鼬模块后，可以使用命令在命令提示符下检查您的**猫鼬**版本。

```
npm mongoose --version
```

**数据库:**这里使用的样本数据库如下所示。

![](img/c39a4a9c77d6e8ab6ef557b5fda6a218.png)

**文件夹结构:**

![](img/3209d9b4369c180282a34be8070d7d6e.png)

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
query.where('loc').within().circle(area)

console.log(query._conditions.loc.$geoWithin)
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
{ '$center': [ [ 20, 20 ], 5 ], '$uniqueDocs': true }
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
var area = { center: [2, 2], radius: 15, unique: true }
query.where('loc').within().circle(area)

console.log(query._conditions.loc.$geoWithin)

app.listen(3000, function(error ) {
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
});
```

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Server listening on PORT 3000
{ '$center': [ [ 2, 2 ], 15 ], '$uniqueDocs': true }
```

**参考:**
[https://mongoosejs . com/docs/API/Query . html # Query _ Query-circle](https://mongoosejs.com/docs/api/query.html#query_Query-circle)