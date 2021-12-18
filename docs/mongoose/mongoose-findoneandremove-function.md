# 猫鼬| findOneAndRemove()功能

> 原文:[https://www . geesforgeks . org/mongose-findonandremove-function/](https://www.geeksforgeeks.org/mongoose-findoneandremove-function/)

**findonandremove()函数**用于根据条件找到元素，然后移除第一个匹配的元素。

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
mongoose.connect('mongodb://127.0.0.1:27017/geeksforgeeks', {
    useNewUrlParser: true,
    useCreateIndex: true,
    useUnifiedTopology: true,
    useFindAndModify: false
});

// User model
const User = mongoose.model('User', {
    name: { type: String },
    age: { type: Number }
});

// Find only one document matching the
// condition(age>=5) and remove it
User.findOneAndRemove({age: {$gte:5} },
                function (err, docs) {
    if (err){
        console.log(err)
    }
    else{
        console.log("Removed User : ", docs);
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![project structure](img/add7ce8f59628f5e57c5b5cc703fb0f4.png)
2.  使用以下命令确保您已经安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是执行函数之前数据库中的示例数据。您可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/18240d1c4e29bb2a150e5b2df055acd1.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/17a84c464a495c3f7f4a4095ebf2062e.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/db0e6e7c16593371cfa83f92484ff72a.png)

这就是如何使用 mongoose findOneAndRemove()函数，该函数根据条件找到文档，然后移除第一个匹配的文档。