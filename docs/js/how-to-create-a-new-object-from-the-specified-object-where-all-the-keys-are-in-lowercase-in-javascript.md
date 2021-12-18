# 如何从指定的对象创建一个新的对象，在 JavaScript 中所有的键都是小写的？

> 原文:[https://www . geeksforgeeks . org/如何从指定对象中创建一个新对象，其中所有键都是小写的 javascript/](https://www.geeksforgeeks.org/how-to-create-a-new-object-from-the-specified-object-where-all-the-keys-are-in-lowercase-in-javascript/)

在本文中，我们将学习如何使用 JavaScript 从指定的对象创建一个新的对象，其中所有的键都是小写的。

**示例:**

> **输入:**{滚动:1，标记:78}
> 
> **输出:**{ rolno:1，mark : 78}

**说明:**这里，我们已经将大写转换为小写键值。

**方法 1:**

一个简单的方法是从 Object 和小写中提取所有键，并用它们创建 Object。为此，我们使用 Object.keys()从对象中提取密钥。并使用 String.toLowerCase()方法来小写键，使用 Array.reduce()方法来制作一个带有小写字符串的对象。

**例 1:**

## 超文本标记语言

```
<script>
  // Test Object
  const Student = { RollNo : 1, Mark: 78 };

  // Function to lowercase keys 
  function Conv( obj , key )
  {
    obj[key.toLowerCase()] = Student[key];
    return Student;
  }

  // Function to  create object from lowercase keys 
  function ObjKeys( obj) {
    let arr1 = Object.keys(obj);
    let ans = {};
    for(let i of arr1)
    {
    Conv(ans,i);

    }
    return ans;
  }

  a = ObjKeys(Student);
  console.log(a);

</script>
```

**输出:**

```
{ rollno : 1, mark : 78}
```

**方法 2:**

最简单的方法是将对象转换为数组，将键转换为小写，并从新数组中创建对象。为此，我们使用 Object.entries()从 Object 创建一个数组。我们使用 Array.map()将 String.toLowerCase()方法应用于所有键。要将新数组转换为对象，我们使用 Object.fromEntries()。

**示例:**

## 超文本标记语言

```
<script>
  // Test Object
  const employ = { EmpId: 101, Batch: 56 };

  // Converting Object to array 
  let k = Object.entries(employ);

  //  Apply toLowerCase function to all keys 
  let l = k.map(function(t){
    t[0] = t[0].toLowerCase()
    return t;
    }
  );

  // Converting back array to Object
  const a  = Object.fromEntries(l)
  console.log(a)
</script>
```

**输出:**

```
{ empid : 101, batch : 56 } 
```