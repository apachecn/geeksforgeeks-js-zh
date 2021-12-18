# Collect.js 有()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-has-method/](https://www.geeksforgeeks.org/collect-js-has-method/)

Collect.js 中的**有()方法**用于检查集合中是否存在密钥。在 **JavaScript** 中，首先将数组转换为集合，然后将函数应用于集合。

**语法** :

```
data.has('key')

```

**参数:**

*   **key** : this parameter holds a new operation value.

**返回值:**该方法返回一个布尔值“真”或“假”。

以下示例说明了 Collect.js 中的**具有()功能**

**示例 1** :在这个示例中，我们取一个集合，然后使用**的 has()函数**检查单个值。

## Javascript

```
// Importing the collect.js module
const collect = require('collect.js');

const collection = collect({
  name : 'GeeksforGeeks',
  Field : 'Education',
  Address : 'Noida',
});

console.log(collection.has('name'));
```

**输出** :

```
true

```

**示例 2** :在这个示例中，我们取一个集合，然后使用**的 has()函数**检查多个值。

## Javascript

```
// Importing the collect.js module
const collect = require('collect.js');

const collection = collect({
  name : 'GeeksforGeeks',
  Field : 'Education',
  Address : 'Noida',
});

console.log(collection.has('name', 'Field', 'Address'));
```

**输出** :

```
true

```

**参考:**T2】https://collect.js.org/api/has.html