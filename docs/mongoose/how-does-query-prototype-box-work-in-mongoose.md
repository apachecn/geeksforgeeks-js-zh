# query . prototype . box()在猫鼬中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-box-work in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-box-work-in-mongoose/)

**Query.prototype.box()** 用于指定$box 条件。使用该功能时，*$地理内*根据网格坐标返回文档。
**语法:**

```
Query.prototype.box()
```

**参数:**该函数有一个数组对象参数，该参数有左上角坐标和右上角坐标。
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

var lower_left = [23, -71]
var upper_right= [12, 11]

query.where('loc').within().box(lower_left, upper_right)
query.box({ ll : lower_left, ur : upper_right})

console.log("Geo Location within: ",
    query._conditions.loc.$geoWithin)
```

项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Geo Location within:  { '$box': [ [ 23, -71 ], [ 12, 11 ] ] }
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

var lower_left = [21, -33]
var upper_right= [-6, 32]

query.where('loc').within().box(lower_left, upper_right)
query.box({ ll : lower_left, ur : upper_right})

console.log("Geo Location is: ",
    query._conditions.loc.$geoWithin)

app.listen(3000, function(error ){
    if(error) console.log(error)
    console.log("Server listening on PORT 3000")
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
Server listening on PORT 3000
Geo Location is:  { '$box': [ [ 21, -33 ], [ -6, 32 ] ] }
```

**参考:**T2】https://mongoosejs.com/docs/api/query.html#query_Query-box