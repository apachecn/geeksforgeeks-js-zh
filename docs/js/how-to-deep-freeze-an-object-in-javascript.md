# 如何在 JavaScript 中深度冻结一个对象？

> 原文:[https://www . geesforgeks . org/如何深度冻结 javascript 中的对象/](https://www.geeksforgeeks.org/how-to-deep-freeze-an-object-in-javascript/)

在本文中，我们将看到 JavaScript 中的对象有什么问题，以及为什么我们需要在 JavaScript 中“深度冻结”一个对象。我们还将学习如何在 JavaScript 中“深度冻结”对象。

**JavaScript 中对象的问题:**我们都知道 JavaScript 对象是可变的。我们如何让它们不可改变？将它们定义为*常量*，但是如果我们将一个 JavaScript 对象声明为*常量，*只会防止该对象作为一个整体被重新分配。我们仍然可以重新分配属性并更改它们的值。

**例 1:**

## 超文本标记语言

```
<script>
  const obj1 = { key1: "val1", key2: "val2", key3: "val3" };
  console.log("Before Change");
  console.log(obj1);
  obj1.key1 = "val";
  console.log("After Change");
  console.log(obj1);
</script>
```

**输出:**

```
"Before Change"
{
 key1: "val1",
 key2: "val2",
 key3: "val3"
}
"After Change"
{
key1: "val",
 key2: "val2",
 key3: "val3"
}
```

**如何修复上述问题？**

我们可以使用 JavaScript 提供的 [Object.freeze()](https://www.geeksforgeeks.org/object-freeze-javascript/) 方法来防止在更新和删除现有属性的同时添加新属性。

**例 2:**

## java 描述语言

```
const obj1={key1:"val1", key2:"val2", key3:"val3"}
console.log("Before Change")
console.log(obj1);
Object.freeze(obj1);
obj1.key1="val";
console.log("After Change")
console.log(obj1);
```

**输出:**

```
"Before Change"
{
key1: "val1",
key2: "val2",
key3: "val3"
}
"After Change"
{
key1: "val1",
key2: "val2",
key3: "val3"
}
```

这不是最好的方法，因为它只创建一个浅的对象冻结，如果对象有一些嵌套对象/数组作为属性，嵌套对象/数组仍然可以修改。

**例 3:**

## 超文本标记语言

```
<script>
  const obj1 = { key1: "val1", 
                 key2: "val2", 
                 key3: ["val3", "val4", "val5"] 
               };

  console.log("Before Change");
  console.log(obj1);
  Object.freeze(obj1);
  obj1.key3[0] = "val";
  obj1.key3[1] = "val";
  obj1.key3[2] = "val";
  console.log("After Change");
  console.log(obj1);
</script>
```

**输出:**这是我们需要为对象创建深度冻结的情况。

```
"Before Change"
{
 key1: "val1",
 key2: "val2",
 key3: ["val3", "val4", "val5"]
}
"After Change"
{
 key1: "val1",
 key2: "val2",
 key3: ["val", "val", "val"]
}
```

**如何实施？**

我们将使用递归来实现对象的深度冻结。这个想法是检查每个属性是否是一个对象。如果属性是一个对象，我们将检查它是否被冻结。如果没有冻结，递归调用该属性的冻结函数。这样，我们将创建对象的深度冻结。

**例 4:**

## 超文本标记语言

```
<script>
  const obj1 = { key1: "val1", 
                 key2: "val2", 
                 key3: ["val3", "val4", "val5"] 
               };

  const deepFreeze = (obj1) => {
    Object.keys(obj1).forEach((property) => {
      if (
        typeof obj1[property] === "object" &&
        !Object.isFrozen(obj1[property])
      )
        deepFreeze(obj1[property]);
    });
    return Object.freeze(obj1);
  };
  deepFreeze(obj1);

  console.log("Before Change");
  console.log(obj1);
  obj1.key3[0] = "val";
  obj1.key3[1] = "val";
  obj1.key3[2] = "val";
  console.log("After Change");
  console.log(obj1);
</script>
```

**输出:**

```
"Before Change"
{
 key1: "val1",
 key2: "val2",
 key3: ["val3", "val4", "val5"]
}
"After Change"
{
 key1: "val1",
 key2: "val2",
 key3: ["val3", "val4", "val5"]
}
```