# query . prototype . cast()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-cast-work-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-cast-work-in-mongoose/)

**Query.prototype.cast()** 函数将该查询强制转换为模型的模式。如果 obj 存在，那么它将被丢弃，而不是这个查询。
**语法:**

```
Query.prototype.cast()
```

**参数:**此功能有一个参数，即要铸造的模型，如果没有设置，则默认为*thi . model*。
**返回值:**此函数返回查询对象。

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

const query = User.find()
var res = query.cast();

console.log("Casted to self:", res)
```

项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Casted to self: {}
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

const query = User.find()
var res = query.cast();

console.log("Self Casting:", res)

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
Self Casting: {}
```

**参考:**T2】https://mongoosejs.com/docs/api/query.html#query_Query-cast