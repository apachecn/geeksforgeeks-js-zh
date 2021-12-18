# 怎么破 _。下划线. js 中的每个()函数？

> 原文:[https://www . geesforgeks . org/how-to-break-_-每个函数都用下划线-js/](https://www.geeksforgeeks.org/how-to-break-_-each-function-in-underscore-js/)

**不可能**破 _。每个功能。原因是 _。每个函数的工作方式与 forEach 函数类似，并模仿其本机行为。除非抛出异常，否则它不允许我们打破循环或逃离循环。但是，可以使用不同的方法，如:

*   Throw an exception
*   _。 Find () function
*   _。 Some () features

**抛出异常:**在获得所需值时，每个人可以抛出一个异常。

**语法:**

```
try {
     _(arrayName).each(function(elementName){
        // your code with condition where 
        // exception is to be thrown
     })
}
catch(exception){
     // dont do anything here
}

```

**示例:**

```
<script>
    var arr = [10, 20, 30, 40];
    var cnt = 0;
    try {
        _(arr).each(function (value) {
            if (value == 30) {
                throw new Error();
            }
            // Write your own code to
            //  use the other values,
            // for example:
            console.log(cnt++);
        })
    }
    catch (e) {
        // Don't do anything here
    }
</script>
```

```
**输出:**0 1
```

这里，当检测到值 30 时抛出异常。否则计数(cnt)增加 1

**_。find()函数:** The _。find()函数可用于在找到所需值时中断循环。结果可以存储在外部变量中。

```
_.find(arayName, function(elementName){
     if(elementName == value){
         return false;
     }
     // Write your own code
}

```

**例:**

```
<script>
    var arr = [10, 20, 30, 40];
    var cnt = 0;
    _.find(arr, function (value) {
        if (value == 30) {
            return false;
        }

        // Write your own code 
        // to use the other values,
        // for example:
        console.log(cnt++);
    });
</script>
```

```
**Output:**0 1
```

这是 _。当值达到 30 时，find()函数返回 false。否则计数(cnt)增加 1

**注意:**也可以包括 catch 块之后的 finally 块。

**_。some()函数:** The _。有些()函数类似于 _。函数，并在检测到所需值时停止遍历列表。结果可以存储在外部变量中。

**语法:**

```
_.some(arayName, function(elementName){
    if(elementName==value){
        return false;
    }

    // Write your own code
}

```

**例:**

```
<script>
    var arr = [10, 20, 30, 40];
    var cnt = 0;
    _.some(arr, function (value) {
        if (value == 30) {
            return false;
        }

        // Write your own code 
        // to use the other values,
        // for example:
        console.log(cnt++);
    });
</script>
```

```
**Output:**0 1
```

这是 _。当检测到值 30 时，some()函数返回 false。否则计数(cnt)增加 1。