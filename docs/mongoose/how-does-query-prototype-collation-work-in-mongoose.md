# query . prototype . collection()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-collection-work in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-collation-work-in-mongoose/)

**query . prototype . collection()**允许用户为各种比较指定特定于语言的规则，如字符串比较，如重音符号规则或字母大小写规则等。
**语法:**

```
Query.prototype.collation()
```

**参数:**这个函数有一个数组参数，即一个对象，它可以有各种属性，如区域设置、案例级别、案例优先等。
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

var query = User.find();
query.collation({ caseFirst:"upper" })

console.log("Collation set to : ", query.options)
```

项目结构会是这样的:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Collation set to :  { collation: { caseFirst: 'upper' } }
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
query.collation({ caseFirst:"upper" })

console.log("Collation : ", query.options)

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
Collation :  { collation: { caseFirst: 'upper' } }
```

**参考:**[https://mongoosejs . com/docs/API/Query . html # Query _ Query-整理](https://mongoosejs.com/docs/api/query.html#query_Query-collation)