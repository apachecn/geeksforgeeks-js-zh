# JavaScript 课程| JavaScript 中的对象

> 原文:[https://www . geesforgeks . org/JavaScript-course-objects-in-JavaScript/](https://www.geeksforgeeks.org/javascript-course-objects-in-javascript/)

**之前的话题:** [JavaScript 课程| JavaScript 中的函数](https://www.geeksforgeeks.org/javascript-course-functions-in-javascript/)
我们已经了解了 JavaScript 提供给我们的不同数据类型，其中大部分是原始的。物体本质上并不原始，理解起来有点复杂。javascript 中的所有东西基本上都是一个对象，这就是为什么很好地理解它们是什么变得非常重要的原因。对象用于存储各种数据和更复杂实体的键控集合。
我们可以通过多种方式创建对象。一种是通过使用带有可选属性列表的方括号{…}。对象的属性采用“键:值”对的形式。另一种方法是使用“new”关键字。
可以使用下面给出的语法创建一个空对象。

```
let person = new Object(); // "object constructor" syntax
let person = {};  // "object literal" syntax

```

这两种方法都是正确，尽管选择什么完全由你决定。我们也可以将属性放入对象中，如:
**示例:**

```
<script>
// an object
let person = {     
  name: "Mukul",  // by key "name" store value "Mukul"
  age: 22        // by key "age" store value 22
};
</script>
```

在上面的例子中，我们有一个名为“人”的简单对象，它有两个属性，即“姓名”和“年龄”，形式为“键:值”对，其中键在冒号的左边，值总是在右边。
创建对象后，我们必须知道如何访问对象的属性，有两种方法可以实现。

```
 objectname.propertyname;  // dot notation
 objectname['propertyname']; // bracket notation

```

第一种方法称为“点标记法”，第二种方法称为“括号标记法”。两者做同样的事情。
**例:**

```
<script>
// getting property values 
let person = {     
  name: "Mukul",  // by key "name" store value "Mukul"
  age: 22        // by key "age" store value 22
};
document.write(person.name+'</br>'); 
document.write(person['age']);
</script>
```

**输出:**

```
Mukul
22 

```

我们可以随时向对象添加属性，就像删除值一样。
**例:**

```
<script>
// an object
let person = {     
  name: "Mukul",  // by key "name" store value "Mukul"
  age: 22        // by key "age" store value 22
};
// adding values to the person object
person.isHappy = 'false';
document.write(person.isHappy);
</script>
```

**输出:**

```
false

```

为了给一个对象添加一个属性，我们只需写下对象的名称，使用点符号并赋值，它就会像上面的例子一样自动添加到对象中。如果我们想删除一个属性，我们使用 delete 关键字，后跟属性访问的正常语法。
**例:**

```
<script>
// an object
let person = {     
  name: "Mukul",  // by key "name" store value "Mukul"
  age: 22        // by key "age" store value 22
};
// adding values to the person object
delete person.age;
document.write(person.age);
</script>
```

**输出:**

```
undefined

```

在上面的代码中，我们删除了人员对象的年龄属性，然后我们尝试将其打印到屏幕上，它将打印“未定义”，因为它不存在。

**遍历一个对象**
遍历一个对象是 javascript 开发人员必须知道的。我们利用..在对象中循环时循环。

```
  for( let Key in person) {
    alert(key) // will print the property key
    alert(person[key]) // will print the value of each key
  }

```

**示例:**

```
<script>
// an object
let person = {     
  name: "Mukul",  // by key "name" store value "Mukul"
  age: 22        // by key "age" store value 22
};
// looping using for..in loop
for( let key in person ) {
 alert(key);
 alert(person[key]);
}
</script>
```

**输出:**

```
name
Mukul
age
22

```

**下一个主题:** [JavaScript 课程|任务跟踪器项目](#)