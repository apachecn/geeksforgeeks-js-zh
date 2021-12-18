# 猫鼬| findOneAndUpdate()功能

> 原文:[https://www . geesforgeks . org/mongose-findonenandupdate-function/](https://www.geeksforgeeks.org/mongoose-findoneandupdate-function/)

**findOneAndUpdate()函数**用于查找匹配的文档并根据更新参数进行更新，传递任意选项，并将找到的文档(如有)返回回调。

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

// Database connection
mongoose.connect('mongodb://127.0.0.1:27017/geeksforgeeks',{
    useNewUrlParser: true,
    useCreateIndex: true,
    useUnifiedTopology: true,
    useFindAndModify: false
});

// User model
const User = mongoose.model('User',{
    name: { type: String },
    age: { type: Number }
});

// Find document matching the condition(age >= 5)
// and update first document with new name='Anuj'
// This function has 4 parameters i.e. filter,
// update, options, callback
User.findOneAndUpdate({age: {$gte:5} }, 
    {name:"Anuj"}, null, function (err, docs) {
    if (err){
        console.log(err)
    }
    else{
        console.log("Original Doc : ",docs);
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![project structure](img/1742a6e2f538c1688e4d90a540581758.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/ee647fa5c3398c6e20569d32785c2772.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/8757a9dc57fff56cff50d7f8408397c3.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/d3721fd03a8a9469ce35b917e5e29b51.png)

这就是如何使用 mongoose findOneAndUpdate()函数，该函数查找匹配的文档并根据更新参数进行更新，传递任何选项，并将找到的文档(如果有)返回给回调。