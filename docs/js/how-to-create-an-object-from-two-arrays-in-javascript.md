# 如何在 JavaScript 中用两个数组创建一个对象？

> 原文:[https://www . geesforgeks . org/如何从 javascript 中的两个数组创建对象/](https://www.geeksforgeeks.org/how-to-create-an-object-from-two-arrays-in-javascript/)

给定两个数组，任务是从它们创建一个对象，其中第一个数组包含对象的键，第二个数组包含对象的值。如果数组长度不同或数组为空，返回 *null* 。现实生活中这个问题的一个例子是，例如，你有一个学生的学号数组和一个学生姓名数组，它们的顺序相同，你想创建一个对象，这样你就可以很容易地使用学号访问学生姓名。

**示例:**

```
Input:
Array 1 =>  [1, 2, 3, 4]
Array 2 =>  ["ram", "shyam", "sita", "gita"]

Output:
{
  1: "ram",
  2: "shyam",
  3: "sita",
  4: "gita"
}
```

为了解决这个问题，我们有以下方法:

**示例 1:** 对每个循环使用。

## java 描述语言

```
let a = [1, 2, 3, 4];
let b = ["ram", "shyam", "sita", "gita"]

// Checking if the array lengths are same 
// and none of the array is empty
 function convertToObj(a, b){
  if(a.length != b.length || a.length == 0 || b.length == 0){
   return null;
  }
  let obj = {};

// Using the foreach method
  a.forEach((k, i) => {obj[k] = b[i]})
  return obj;
}
console.log(convertToObj(a, b))
```

**输出:**

```
{
  1: "ram",
  2: "shyam",
  3: "sita",
  4: "gita"
}
```

**示例 2:** 使用对象分配方法。

## java 描述语言

```
let a = [1, 2, 3, 4];
let b = ["ram", "shyam", "sita", "gita"]

// Checking if the array lengths are same 
// and none of the array is empty
 function convertToObj(a, b){
  if(a.length != b.length || a.length == 0 || b.length == 0){
    return null;
  }

// Using Object.assign method
  return Object.assign(...a.map((k, i)=>({[k]: b[i]}) ))
}
console.log(convertToObj(a, b))
```

**输出:**

```
{
  1: "ram",
  2: "shyam",
  3: "sita",
  4: "gita"
}
```