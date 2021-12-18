# query . prototype . equals()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-equal-work in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-equals-work-in-mongoose/)

**Query.prototype.equals()** 函数用于指定用 where()函数指定的路径的互补比较值。
**语法:**

```
Query.prototype.equals()
```

**参数:**该功能有一个对象类型的*值*参数。
**返回值:**此函数返回查询对象。
安装猫鼬:

```
npm install mongoose
```

安装猫鼬模块后，可以使用命令在命令提示符下检查您的**猫鼬**版本。

```
npm mongoose --version
```

现在，创建一个文件夹并添加一个文件，例如 index.js，如下所示。

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

var query = User.find({});
query.where('age').equals(5)
  .exec(function(err, res){
    if(err) console.log(err)
    console.log(res)
})
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

var query = User.find({});
query.where('age').equals(25).exec(function(err, res){
    if(err) console.log(err)
    console.log(res)
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

> 在 PORT 3000 上侦听的服务器
> [{ _ id:5ebc 3669 a 99 bde 77 B2 efb 9 ba，名称:‘Lalit’，年龄:25，__v: 0 } ]

**参考:**
[https://mongoosejs . com/docs/API/Query . html # Query _ Query-equals](https://mongoosejs.com/docs/api/query.html#query_Query-equals)