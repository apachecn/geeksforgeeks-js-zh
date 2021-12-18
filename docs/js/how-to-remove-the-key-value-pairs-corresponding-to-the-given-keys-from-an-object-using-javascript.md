# 如何使用 JavaScript 从对象中移除给定键对应的键值对？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 从对象中移除对应于给定键的键值对/](https://www.geeksforgeeks.org/how-to-remove-the-key-value-pairs-corresponding-to-the-given-keys-from-an-object-using-javascript/)

在 JavaScript 中，对象以键值对的形式存储数据，其中键可以是对象的任何属性。在本文中，让我们看看如何移除对象中对应于给定键的**键值**对。

使用**删除**运算符。当只删除一个键时，我们可以直接使用 delete 操作符指定对象中的键。

**语法:**

```
delete(object_name.key_name);
/* or */
delete(object_name[key_name]);
```

**示例:**

## 超文本标记语言

```
<script>
      var myObj = {
        Name: "Raghav",
        Age: 30,
        Sex: "Male",
        Work: "Web Developer",
        YearsOfExperience: 6,
        Organisation: "GeeksforGeeks",
        Address: "address--address some value"
      };

      console.log("After removal: ");
      // Deleting address key
      delete (myObj.Address); // Or delete(myObj[Address]);
      console.log(myObj);
</script>    
```

**输出:**

```
"After removal: "
[object Object] {
  Age: 30,
  Name: "Raghav",
  Organisation: "GeeksforGeeks",
  Sex: "Male",
  Work: "Web Developer",
  YearsOfExperience: 6
}
```

当**多个键**要被移除时，这些键可以被存储在一个**数组**中，并且可以被传递给一个函数，该函数使用一个循环来删除数组中所需的键。

**语法:**

```
function function_name(object_name, array_of_keys) {
    { Iterate through the array using loop. }
    return object_name;
}
```

**例 2:**

## 超文本标记语言

```
<script>
    // Function to delete the keys given in the array
    function DeleteKeys(myObj, array) {
      for (let index = 0; index < array.length; index++) {
          delete myObj[array[index]];
      }
      return myObj;
    }

    // Declaring the object
    var myObj = {
      Name: "Raghav",
      Age: 30,
      Sex: "Male",
      Work: "Web Developer",
      YearsOfExperience: 6,
      Organisation: "Geeks For Geeks",
      Address: "address--address some value"
    };

    // Adding the keys to be deleted in the array
    var array = 
    ["Work", "Address", "Organisation", "YearsOfExperience"];
    var finalobj = DeleteKeys(myObj, array);
    console.log("After removal: ");
    console.log(finalobj);
</script>
```

**输出:**

```
"After removal: "
[object Object] {
  Age: 30,
  Name: "Raghav",
  Sex: "Male"
}
```