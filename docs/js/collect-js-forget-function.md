# Collect.js |忘本()功能

> 原文:[https://www.geeksforgeeks.org/collect-js-forget-function/](https://www.geeksforgeeks.org/collect-js-forget-function/)

**忘记()**功能，如名称所示，使用其键忘记/移除收藏中的项目。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。
**语法:**

```
data.forget('key')
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **键:**该参数保存定义该键的值的键名。

**返回值:**返回集合，除了提到的键的值。

下面的例子说明了 collect.js
**中的**忘带()**函数示例 1:** 在本例中，我们取一个集合，然后使用**忘带()**函数返回没有忘记的关键元素的集合。

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const collection = collect({
  name: 'Jhon',
  Roll: 7,
});

collection.forget('Roll');

console.log(collection.all());
```

**输出:**

```
{ name: 'Jhon' }

```

**示例 2:** 我们在这里做的事情与上面的示例相同。

## 蟒蛇 3

```
// It is used to import collect.js library
const collect = require('collect.js');

const collection = collect({
  Address : '253 Steet , California',
  pincode : '0987'
});

collection.forget('Address');

console.log(collection.all());
```

**输出:**

```
{ pincode: '0987' }

```

**参考文献:**T2**https://collect.js.org/api/forget.html**T5】