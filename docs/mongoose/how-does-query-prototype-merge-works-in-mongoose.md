# query . prototype . merge()在 Mongoose 中是如何工作的？

> 原文:[https://www . geesforgeks . org/how-do-query-prototype-merge-works-in-mongose/](https://www.geeksforgeeks.org/how-does-query-prototype-merge-works-in-mongoose/)

**Query.prototype.merge()** 函数用于将另一个 Query 或 conditions 对象合并到当前使用该函数的查询中，即*这个*查询。当查询通过时，条件、字段选择和选项将被合并。
**语法:**

```
Query.prototype.merge()
```

**参数:**该功能有一个*源*参数为对象/查询类型。
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

const query = User.find({age: { $gte:0 }})

console.log("Before merge function")
query.exec(function(err, res){
    if(err) console.log(err)
    else console.log(res)
});

setTimeout(function() {

   query.merge({name:"Gourav"})

   console.log("After merge function")  
   query.exec(function(err, res){
     if(err) console.log(err)
     else console.log(res)
   });

}, 1000);
```

项目结构会是这样的:

![](img/3209d9b4369c180282a34be8070d7d6e.png)

使用以下命令运行 **index.js** 文件:

```
node index.js
```

**输出:**

> 合并功能前
> [
> { _ id:5 ebb 9129 a 99 bde 77 B2 efb 809，姓名:' Gorav '，年龄:10，__v: 0 }，
> { _ id:5 ebc 3669 a 99 bde 77 B2 efb 9 ba，姓名:' Lalit '，年龄:25，__v: 0 }，
> { _ id:5 ebc 367 da 99 bde 77 B2 efb 9 BF，姓名:' Piyush '，年龄:5，_ _

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

const query = User.find({age: { $gte: 1}})

console.log("Before merge function")
query.exec(function(err, res){
    if(err) console.log(err)
    else console.log(res)
});

setTimeout(function() {

   query.merge({name:"Gourav"})

   console.log("After merge function")  
   query.exec(function(err, res){
     if(err) console.log(err)
     else console.log(res)
   });

}, 1001);

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

> 合并功能前
> 服务器监听 PORT 3000
> [
> { _ id:5 ebb 9129 a 99 bde 77 B2 efb 809，名称:' gorav '，年龄:10，__v: 0 }，
> { _ id:5 ebc 3669 a 99 bde 77 B2 efb 9 ba，名称:' Lalit '，年龄:25，__v: 0 }，
> { _ id:5 ebc 367 da 99 bde 77 B2 efb 9 BF，

***参考:**[*https://mongoosejs . com/docs/API/Query . html # Query _ Query-merge*](https://mongoosejs.com/docs/api/query.html#query_Query-merge)*