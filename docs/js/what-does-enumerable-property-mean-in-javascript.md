# 可枚举属性在 JavaScript 中是什么意思？

> 原文:[https://www . geeksforgeeks . org/什么是可枚举属性在 javascript 中的含义/](https://www.geeksforgeeks.org/what-does-enumerable-property-mean-in-javascript/)

JavaScript 中的可枚举属性意味着，如果使用 for…in 循环或 Object.keys()方法迭代属性，则可以查看该属性。默认情况下，通过简单赋值或属性初始值设定项创建的所有属性都是可枚举的。

**例 1:**

```
<script>
// Creating a student object
const student = {
    registration: '12342',
    name: 'Sandeep',
    age: 27,
    marks: 98
};

// prints all the keys in student object
for (const key in student) {
    console.log(key);
}
</script>
```

**输出:**

```
registration
name
age
marks

```

**示例 2:** 由于所有属性都是由属性初始化器初始化的，因此默认情况下，它们都将可枚举设置为 true。要显式更改属性的内部可枚举属性，请使用**对象.定义属性()**方法。另外，为了检查一个属性是否可枚举，我们使用函数**properties isenumerable()**。如果属性可枚举，则返回 true，否则返回 false。

```
<script>
// Creating a student object
const student = {
    registration: '12342',
    name: 'Sandeep',
    age: 27,
};

// This sets the enumerable attribute
// of marks property to false 

Object.defineProperty(student, 'marks', {
    value: 98,
    configurable: true,
    writable: false,
    enumerable: false,
});

// To print whether enumerable or not
console.log(student.propertyIsEnumerable('registration')); 
console.log(student.propertyIsEnumerable('name'));
console.log(student.propertyIsEnumerable('age'));
console.log(student.propertyIsEnumerable('marks'));
</script>
```

**输出:**

```
true
true
true
false

```

**注意:**使用 defineProperty()方法创建的属性将可枚举标志设置为 false。当使用 for 循环运行上述代码时，“marks”属性不可见。

```
// This will not print the property 
// Who's enumerable property is set to false

for (const key in student){
    console.log(key)
}

```

**输出:**

```
registration
name
age

```