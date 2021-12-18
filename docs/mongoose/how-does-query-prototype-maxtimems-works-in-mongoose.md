# query . prototype . maxtimems()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-maxtimems-works-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-maxtimems-works-in-mongoose/)

**query . prototype . maxTimeMS()**功能用于设置 maxTimeMS 选项。基本上，如果查询或写操作已经运行超过*毫秒*毫秒，这个函数告诉 MongoDB 服务器中止。

**语法:**

```
Query.prototype.maxTimeMS()
```

**参数:**该功能有一个*毫秒*参数，用于定义毫秒数。
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

const query = User.find();
query.maxTimeMS(10000);

query.exec(function(err,res){
    if(err) console.log(err.message)
    else console.log(res)
})
```

项目结构会是这样的:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
[
  { _id: 5ebb9129a99bde77b2efb809, name: 'Gourav', age: 10, __v: 0 },
  { _id: 5ebc3669a99bde77b2efb9ba, name: 'Lalit', age: 25, __v: 0 },
  { _id: 5ebc367da99bde77b2efb9bf, name: 'Piyush', age: 5, __v: 0 },
  { _id: 5ebd345f5d2d8a3534b2f391, name: 'Manish', age: 34, __v: 0 }
]
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
query.maxTimeMS(30000);

console.log(query.options)

query.exec(function(err,res){
    if(err) console.log(err.message)
    else console.log(res)
})

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
{ maxTimeMS: 10000 }
Server listening on PORT 3000
[
  { _id: 5ebb9129a99bde77b2efb809, name: 'Gourav', age: 10, __v: 0 },
  { _id: 5ebc3669a99bde77b2efb9ba, name: 'Lalit', age: 25, __v: 0 }, 
  { _id: 5ebc367da99bde77b2efb9bf, name: 'Piyush', age: 5, __v: 0 }, 
  { _id: 5ebd345f5d2d8a3534b2f391, name: 'Manish', age: 34, __v: 0 } 
]
```

**参考:**[https://mongoosejs . com/docs/API/Query . html # Query _ Query-maxTimeMS](https://mongoosejs.com/docs/api/query.html#query_Query-maxTimeMS)T4】