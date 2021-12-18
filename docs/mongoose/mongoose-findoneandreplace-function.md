# 猫鼬| findOneAndReplace()功能

> 原文:[https://www . geesforgeks . org/mongose-findonandreplace-function/](https://www.geeksforgeeks.org/mongoose-findoneandreplace-function/)

**findonandreplace()函数**用于查找匹配的元素，用提供的元素替换，并将返回的单据传递给回调。

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
    useUnifiedTopology: true
});

// User model
const User = mongoose.model('User', {
    name: { type: String },
    age: { type: Number }
});

var new_user = {
    name: "ABC",
    age:100
}

// Find document matching the condition(age >= 5)
// and replace first document with above new_user
// This function has 4 parameters i.e. filter,
// replacement, options, callback
User.findOneAndReplace({age: {$gte:5} }, 
         new_user, null, function (err, docs) {
    if (err){
        console.log(err)
    }
    else{
        console.log("Original Doc : ", docs);
    }
});
```

**运行程序的步骤:**

1.  项目结构会是这样的:
    ![project structure](img/50186c6e5489eb86b31a596bf6f9815f.png)
2.  确保您已经使用以下命令安装了猫鼬模块:

    ```
    npm install mongoose
    ```

3.  下面是函数执行前数据库中的样本数据，你可以使用任何 GUI 工具或终端查看数据库，就像我们已经使用的 Robo3T GUI 工具如下所示:
    ![Database](img/b4670f1b08cbbbf0f29e67e613b13312.png)
4.  Run index.js file using below command:

    ```
    node index.js
    ```

    ![](img/b93885544e94c50c221cac0ae9f6b17b.png)

5.  执行该功能后，可以看到如下所示的数据库:
    ![new Database](img/a1a304b740742d3ccfdaec808c276878.png)

这就是如何使用 mongoose findOneAndReplace()函数，该函数查找匹配的文档，用提供的文档替换它，并将返回的文档传递给回调。