# JavaScript 中的冻结和封存有什么区别？

> 原文:[https://www . geeksforgeeks . org/JavaScript 中的冻结和密封的区别是什么/](https://www.geeksforgeeks.org/what-is-the-difference-between-freeze-and-seal-in-javascript/)

**冻结**和**密封**都是用来在 JavaScript 中创建不可扩展的对象，但是它们之间有很多不同之处。 **Object.seal()** 允许更改对象的现有属性，而 **Object.freeze()** 不允许。 **Object.freeze()** 使一个物体对任何事物都免疫，即使很小的变化也不能被改变。 **Object.seal()** 防止删除现有属性，但不能防止外部更改。

**语法:**

```
Object.freeze(objectname);

```

**示例 1:** 描述 **Object.seal()** 的实现。

```
<script>
    // creates an object
    var obj = {
        // assigns 10 to value 
        value: 10
    };
    // creates a non-extensible object
    Object.seal(obj);
    // the value gets updated to 20
    obj.value = 20;
    console.log(obj.value);
</script>
```

**输出:**

```
20

```

**示例-1** 描述了如何使用 **Object.seal()** 创建一个不可扩展的对象，但这并不妨碍对象的值被更改，可以看到该值被更新为 20。

**语法:**

```
Object.seal(objectname);
```

**示例 2:** 描述了**对象冻结()**的实现。

```
<script>
    // creates an object
    var obj = {
        // assigns 10 to value 
        value: 10
    };
    // creates a non-extensible object
    Object.freeze(obj);
    // updates the value
    obj.value = 20;
    // but cannot change the existing value
    console.log(obj.value);
</script>
```

**输出:**

```
10
```

**示例-2** 描述了如何使用 **Object.freeze()** 创建一个不可扩展的对象，但是该对象的现有值被阻止更改，并给出 10 作为输出。