# JavaScript object . prototype . value of()方法

> 原文:[https://www . geesforgeks . org/JavaScript-object-prototype-value of-method/](https://www.geeksforgeeks.org/javascript-object-prototype-valueof-method/)

在 JavaScript 中，Object.prototype.valueOf()方法用于返回指定对象的基元值。每当需要一个基元值时，JavaScript 就会自动调用 valueOf()方法。方法的值会被 JavaScript 中的每个对象自动继承。每个对象重写此方法以返回适当的基元值。如果这个对象没有原始值，那么 JavaScript 返回对象本身。我们可以重写此方法，将任何内置对象转换为基元值。在自定义对象类型的情况下，我们重写此方法来调用自定义方法。

如果我们正在处理自定义对象类型，我们可以使用以下语法为其重写 valueOf()方法:

#### 语法:

```
ObjectType.prototype.valueOf = function() { 
    return CustomPrimitiveValue; 
};
```

在这个语法中，

*   **对象类型:**用户创建的自定义对象类型。
*   **CustomPrimitiveValue:** 指定对象的基元值。

虽然 valueOf()方法是在 JavaScript 中自动调用的，但是我们可以使用以下语法自己调用它:

#### **语法:**

```
ObjectType.valueOf()
```

#### **示例:**

## Java Script 语言

```
<script>
    function myFunction() {

        // Creating a custom object
        // type ExType
        function ExType(n) {
            this.number = n;
        }

        // A callback method overriding
        // the valueOf() method
        ExType.prototype.valueOf = function () {

            // Returned valued is 18+3 which is 21
            return this.number + 3;
        };

        // Creating an object of ExType object type
        const object1 = new ExType(18);

        // Logs 21-12 which is 9
        console.log(object1 - 12);
    }

    myFunction();
</script>
```

#### **输出:**

![](img/1d04feb6e54ca73f82913dbb179a2dc6.png)

在上面的示例中，我们试图重写 valueOf()方法，以实际数字加 3 的形式返回基元值。因此，当参数为 21 时，传递 18 后返回的原始值。当我们试图记录原始值减 12 时，我们得到了 21-12，即 9 作为我们的最终答案。