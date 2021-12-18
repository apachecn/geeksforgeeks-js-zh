# 如何在 JavaScript 中比较两个对象，确定第一个对象包含与第二个对象等价的属性值？

> 原文:[https://www . geesforgeks . org/如何比较两个对象-确定第一个对象-包含等价属性值-第二个对象-在 javascript 中/](https://www.geeksforgeeks.org/how-to-compare-two-objects-to-determine-the-first-object-contains-equivalent-property-values-to-the-second-object-in-javascript/)

给定两个对象 **obj1** 和 **obj2** ，任务是检查 **obj1** 是否包含 JavaScript 中 **obj2** 的所有属性值。

```
Input: obj1: { name: "John", age: 23; degree: "CS" }
       obj2: {age: 23, degree: "CS"}

Output: true

Input: obj1: { name: "John", degree: "CS" }
       obj2: {name: "Max", age: 23, degree: "CS"}

Output: false
```

为了解决这个问题，我们遵循以下方法。

**方法 1:** 解决这个问题是一种**天真的**方法。在这种方法中，我们使用**来迭代**对象 2** ..在**循环中，每次迭代时，我们检查两个对象的当前键是否相等，我们返回 **false** 否则循环完成后我们返回 **true** 。

**示例:**

## java 描述语言

```
<script>

    // Define the first object
    let obj1 = {
        name: "John",
        age: 23,
        degree: "CS"
    }

    // Define the second object
    let obj2 = {
        age: 23,
        degree: "CS"
    }

    // Define the function check
    function check(obj1, obj2) {

        // Iterate the obj2 using for..in
        for (key in obj2) {

            // Check if both objects do 
            // not have the equal values
            // of same key
            if (obj1[key] !== obj2[key]) {
                return false;
            }
        }
        return true
    }

    // Call the function
    console.log(check(obj1, obj2))
</script>
```

**输出:**

```
true
```

**方法 2:** 在该方法中，我们使用 **Object.keys()** 方法创建 obj2 的所有键的数组，然后使用 **Array.every()** 方法检查 obj2 的所有属性是否等于 obj1。

**示例:**

## java 描述语言

```
<script>

    // Define the first object
    let obj1 = {
        name: "John",
        age: 23,
        degree: "CS"
    }

    // Define the Second object
    let obj2 = {
        age: 23,
        degree: "CS"
    }

    // Define the function check
    function check(obj1, obj2) {
        return Object

            // Get all the keys in array
            .keys(obj2)
            .every(val => obj1.hasOwnProperty(val) 
                && obj1[val] === obj2[val])
    }

    // Call the function
    console.log(check(obj1, obj2))
</script>
```

**输出:**

```
true
```