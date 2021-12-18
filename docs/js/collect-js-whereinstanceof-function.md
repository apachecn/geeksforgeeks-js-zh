# Collect.js whereInstanceOf()函数

> 原文:[https://www . geesforgeks . org/collect-js-where instance of-function/](https://www.geeksforgeeks.org/collect-js-whereinstanceof-function/)

**whereInstanceOf()** 函数用于过滤给定类别类型的输入。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.whereInstanceOf('key')

```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **键:**该参数保存定义该键的值的键名。

**返回值:**用提到的键值返回集合。
下面的示例说明了 collect.js 中的 **whereInstanceOf()** 函数
**示例 1:** 在此示例中，我们获取一个集合，然后使用 **whereInstanceOf()** 方法使用键返回过滤后的集合。

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const Input = collect([
  new Books('Pride and prejudice'),
  new Books('The Great Gatsby '),
  new Movies('It'),
]);

const output = Input.whereInstanceOf(Books);
console.log(output.all());
```

**输出:**

```
[
   new Books('Pride and prejudice'),
   new Books('The Great Gatsby'),
]

```

**例 2:** 我们这里做的和上面的例子一样。

## java 描述语言

```
// It is used to import collect.js library
const collect = require('collect.js');

const Input = collect([
  new Year('1980'),
  new Year('2020'),
  new Name('Mohan'),
]);

const output = Input.whereInstanceOf(Name);

console.log(output.all());
```

**输出:**

```
[
  new Name('Mohan'),
]

```

**参考文献:**T2**https://collect.js.org/api/whereinstanceof.html**T5】