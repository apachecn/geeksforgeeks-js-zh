# 在 JavaScript 中如何统计对象数组中重复名字出现的次数？

> 原文:[https://www . geesforgeks . org/如何计算 javascript 对象数组中重复名称的出现次数/](https://www.geeksforgeeks.org/how-to-count-number-of-occurrences-of-repeated-names-in-an-array-of-objects-in-javascript/)

给定一个对象数组，任务是根据给定键的值查找它的出现。

**示例:**

```
Input : arr = [
   {
      employeeName: "Ram",
      employeeId: 23
   },
   {
      employeeName: "Shyam",
      employeeId: 24
   },
   {
      employeeName: "Ram",
      employeeId: 21
   },
   {
      employeeName: "Ram",
      employeeId: 25
   },
   {
      employeeName: "Kisan",
      employeeId: 22
   },
   {
      employeeName: "Shyam",
      employeeId: 20
   }
]

key = "employeeName"

Output: [
    {employeeName: "Ram", occurrences: 3},
    {employeeName: "Shyam", occurrences: 2},
    {employeeName: "Kisan", occurrences:  1}
] 
```

为此，我们有以下方法:

#### 方法 1:

在这种方法中，我们遵循以下步骤。

*   创建一个空输出数组。
*   使用 forEach 迭代输入数组。
*   检查输出数组是否包含任何包含提供的键值的对象
*   如果没有，则创建一个新对象，并使用设置为值(当前迭代对象的键的值)的键(提供的键名)和设置为值 1 的事件初始化该对象
*   如果是，则迭代输出数组并搜索当前迭代的键是否等于输入数组迭代的键，然后将出现次数增加到 1。

## java 描述语言

```
<script>
function findOcc(arr, key){
  let arr2 = [];

  arr.forEach((x)=>{

    // Checking if there is any object in arr2
    // which contains the key value
     if(arr2.some((val)=>{ return val[key] == x[key] })){

       // If yes! then increase the occurrence by 1
       arr2.forEach((k)=>{
         if(k[key] === x[key]){ 
           k["occurrence"]++
         }
      })

     }else{
       // If not! Then create a new object initialize 
       // it with the present iteration key's value and 
       // set the occurrence to 1
       let a = {}
       a[key] = x[key]
       a["occurrence"] = 1
       arr2.push(a);
     }
  })

  return arr2
}

let arr = [
   {
      employeeName: "Ram",
      employeeId: 23
   },
   {
      employeeName: "Shyam",
      employeeId: 24
   },
   {
      employeeName: "Ram",
      employeeId: 21
   },
   {
      employeeName: "Ram",
      employeeId: 25
   },
   {
      employeeName: "Kisan",
      employeeId: 22
   },
   {
      employeeName: "Shyam",
      employeeId: 20
   }
]

let key = "employeeName"
console.log(findOcc(arr, key))
</script>
```

**输出:**

```
[
   {
      employeeName: "Ram",
      occurrence: 3
   }, 
   {
      employeeName: "Shyam",
     occurrence: 2
   }, 
   {
    employeeName: "Kisan",
    occurrence: 1
   }
]
```