# 如何在 JavaScript 中获取对象的属性描述符？

> 原文:[https://www . geesforgeks . org/如何获取 javascript 中对象的属性描述符/](https://www.geeksforgeeks.org/how-to-get-property-descriptors-of-an-object-in-javascript/)

在这里，我们将讨论 JavaScript 中对象的属性描述符。方法返回一个描述给定对象的特定属性的对象。可以用多种方式创建一个 JavaScript 对象，并且可以通过使用该对象的属性描述符来调用它的属性。

**语法:**

```
Object.getOwnPropertyDescriptor( obj, prop )
```

object . getowntpropertysdescriptor()接受两个参数作为输入，如下所述:

*   **obj** :是指要描述属性的对象名称。
*   **prop** :定义要返回值的对象中的特定属性。

**返回值:**该方法返回对象的属性(如果存在的话)，否则返回未定义。

**示例:**在下面的示例中，创建了一个由两个属性 property1 和 property2 组成的对象 Obj。我们使用**object . getowntpropertysdescriptor()**属性返回与每个属性相关的属性和值。

## Java Script 语言

```
<script>

    // Object
    const Obj = {
        property1: "GeeksforGeeks",
        property2: 12
    };

    const descriptor1 = Object
        .getOwnPropertyDescriptor(Obj, 'property1');

    const descriptor2 = Object
        .getOwnPropertyDescriptor(Obj, 'property2');

    console.log(descriptor1.configurable);
    // expected output: true

    console.log(descriptor1.enumerable);
    // expected output: true

    console.log(descriptor1.value);
    // expected output: GeeksforGeeks

    console.log(descriptor2.value);
    // expected output: 12

</script>
```

**输出:**

```
true
true
GeeksforGeeks
12
```

### 描述符:

对象的属性描述符由定义每个属性的下列属性组成:

*   **值:**是与被调用的属性相关联的值
*   **可写:**表示属性是否可以更改。只有当属性可以被操作时，它才返回 true
*   **可枚举:**如果在枚举对应对象的属性时属性可见，则返回 true。
*   **可配置:**表示属性描述符是否可以从相应对象中更改或移除。

**示例:**以下示例描述了与对象 Obj 相关的属性 1 和属性 2 的属性属性。

## Java Script 语言

```
<script>
    const Obj = {
        property1: "GeeksforGeeks",
        property2: 12
    };

    const descriptor1 = Object
        .getOwnPropertyDescriptor(Obj, 'property1');

    const descriptor2 = Object
        .getOwnPropertyDescriptor(Obj, 'property2');

    console.log(descriptor1);
    console.log(descriptor2);
</script>
```

**输出:**

```
{value: 'GeeksforGeeks', writable: true, enumerable: true, configurable: true}
    configurable: true
    enumerable: true
    value: "GeeksforGeeks"
    writable: true
    [[Prototype]]: Object

{value: 12, writable: true, enumerable: true, configurable: true}
    configurable: true
    enumerable: true
    value: 12
    writable: true
    [[Prototype]]: Object
```