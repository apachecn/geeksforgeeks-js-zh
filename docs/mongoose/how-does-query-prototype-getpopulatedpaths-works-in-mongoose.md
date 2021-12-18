# query . prototype . getpopulatedpaths()在猫鼬中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-getpopulatedpaths-works-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-getpopulatedpaths-works-in-mongoose/)

**query . prototype . GetPopulatedPaths()**函数用于获取此查询要填充的路径列表。表示填充路径的字符串数组作为参数传递。

**语法:**

```
Query.prototype.getPopulatedPaths()
```

**参数:**该函数有一个数组参数，该参数是表示填充路径的字符串数组。
**返回值:**该函数返回查询对象。

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

const query = User.find().populate({
    path: 'level2',
    populate: { path: 'level3' }
});

console.log("Populate:", query.getPopulatedPaths());
```

项目结构会是这样的:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

```
Populate: [ 'level2', 'level2.level3' ]
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

const query = User.find().populate({
    path: 'level2',
    populate: { path: 'level3' }
});

console.log("Populate:", query.getPopulatedPaths());

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
Server listening on PORT 3000
Populate: [ 'level2', 'level2.level3' ]
```

**参考:**T2T4】