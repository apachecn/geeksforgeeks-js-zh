# query . prototype . map()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-map-works-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-map-works-in-mongoose/)

**Query.prototype.map()** 函数用于运行函数 fn，并将 fn 的返回值视为查询要解析的新值。传递给 map() 函数的所有函数都将在任何一个 post hooks 之后运行。

**语法:**

```
Query.prototype.map()
```

**参数:**这个函数有一个参数 *fn* ，是运行来转换查询结果的函数。
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

这里，文件名是 index.js

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

const query = User.find({name:"Lalit"}).map(res => {

  console.log("loadedAt property set on the doc "
       + "to tell the time doc was loaded.")
  return res == null ? res : Object.assign(res,
       { loadedAt: new Date() });
});

query.exec(function(err, res){
    if(err) console.log(err)
    else console.log(res)
});
```

项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
loadedAt property set on the doc to tell the time doc was loaded.
[
  { _id: 5ebc3669a99bde77b2efb9ba, name: 'Lalit', age: 25, __v: 0 },
  loadedAt: 2020-07-14T18:22:57.991Z
]
```

**例 2:**

这里，文件名是 index.js

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

const query = User.find().map(res => {

 console.log("loadedAt property set on the doc "
      + "to tell the time doc was loaded.")
 return res == null ? res : Object.assign(res,
      { loadedAt: new Date() });

});

query.exec(function(err, res){
    if(err) console.log(err)
    else console.log(res)
});

app.listen(3000, function(error ) {
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
});
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
Server listening on PORT 3000
loadedAt property set on the doc to tell the time doc was loaded.
[
  { _id: 5ebb9129a99bde77b2efb809, name: 'Gourav', age: 10, __v: 0 },
  { _id: 5ebc3669a99bde77b2efb9ba, name: 'Lalit', age: 25, __v: 0 }, 
  { _id: 5ebc367da99bde77b2efb9bf, name: 'Piyush', age: 5, __v: 0 }, 
  { _id: 5ebd345f5d2d8a3534b2f391, name: 'Manish', age: 34, __v: 0 },
  loadedAt: 2020-07-14T18:24:36.890Z
]
```

**参考:**T2https://mongoosejs.com/docs/api/query.html#query_Query-map