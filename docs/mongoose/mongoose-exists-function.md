# 猫鼬|存在()功能

> 原文:[https://www.geeksforgeeks.org/mongoose-exists-function/](https://www.geeksforgeeks.org/mongoose-exists-function/)

如果数据库中至少存在一个与给定过滤器匹配的文档，则 **exists()函数**返回 true，否则返回 false。

**猫鼬模块安装:**

1.  您可以访问[安装猫鼬模块](https://www.npmjs.com/package/mongoose)的链接。您可以使用此命令安装此软件包。

    ```
    npm install mongoose
    ```

2.  安装猫鼬模块后，您可以使用命令在命令提示符下检查您的猫鼬版本。

    ```
    npm version mongoose
    ```

3.  之后，您可以创建一个文件夹并添加一个文件，例如 index.js。

    ```
    node index.js
    ```

**文件名:index.js**

```
const mongoose = require('mongoose');

// Database Connection
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

User.exists({name:'Gourav'}, function (err, doc) {
    if (err){
        console.log(err)
    }else{
        console.log("Result :", doc) // false
    }
});

User.exists({name:'Amit'}, function (err, doc) {
    if (err){
        console.log(err)
    }else{
        console.log("Result :", doc) // true
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![](img/cbb1c85b8e0673efff3befb63eb0b22b.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![](img/ac37f3072f3c07dd1ec8e9298f367221.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/0bd3d1e63ebd09b5811170080e1a96c7.png)

这就是如何使用 mongoose exists()函数，如果数据库中至少有一个文档与给定的过滤器匹配，则返回 true，否则返回 false。