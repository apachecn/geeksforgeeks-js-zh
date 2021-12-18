# query . prototype . all()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-all-work in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-all-work-in-mongoose/)

**Query.prototype.all()** 指定了一个$all 查询条件。用户可以指定在作为参数传递的数组中必须匹配的所有值。
**语法:**

```
Query.prototype.all()
```

**参数:**这个函数有两个参数，路径和值数组。
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

User.find().all('name',['Gourav'])
.exec(function(error, result) {
    if (error) {
        console.log(error)
    } else {
        console.log(result)
    }
});
```

项目结构如下所示:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

> [ { _id: 5ebb9129a99bde77b2efb809，名称:“gourav”，年龄:10，_ _ _ _ _ _ _ _ v:0 }]

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

User.find().all('age', [25])
.exec(function(error, result) {
    if (error) {
        console.log(error)
    } else {
        console.log(result)
    }
});

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

> 在 PORT 3000 上侦听的服务器
> [{ _ id:5ebc 3669 a 99 bde 77 B2 efb 9 ba，名称:‘Lalit’，年龄:25，__v: 0 } ]

**参考:**T2】https://mongoosejs.com/docs/api/query.html#query_Query-all