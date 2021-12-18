# JavaScript |命名空间

> 原文:[https://www.geeksforgeeks.org/javascript-namespace/](https://www.geeksforgeeks.org/javascript-namespace/)

**命名空间**是指为标识符(类型、函数、变量等的名称)提供范围以防止它们之间冲突的编程范式。例如，在不同的上下文中，程序可能需要相同的变量名。在这种情况下使用名称空间将隔离这些上下文，以便相同的标识符可以在不同的名称空间中使用。在本文中，我们将讨论如何在 JavaScript 中初始化和使用名称空间。默认情况下，JavaScript 不提供命名空间。然而，我们可以通过创建一个包含所有函数和变量的全局对象来复制这个功能。

**语法:**

*   Initialize an empty namespace

    ```
     var <namespace> = {}; 
    ```

*   Access namespace

    ```
     <namespace>.<identifier> 
    ```

中的变量

下面的例子说明了 JavaScript 中的**命名空间**:

**示例:**如下图，标识符`startEngine`用于表示汽车和自行车对象中的不同功能。以这种方式，我们可以通过将相同的标识符附加到不同的全局对象来在不同的名称空间中使用它。

```
<script>
var car = {
    startEngine: function () {
        console.log("Car started");             
    }        
}

var bike = {
    startEngine: function () {
        console.log("Bike started");
    }
}

car.startEngine();
bike.startEngine();
</script>
```

**输出:**

```
Car started
Bike started
```