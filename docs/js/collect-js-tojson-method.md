# Collect.js toJson()方法

> 原文:[https://www.geeksforgeeks.org/collect-js-tojson-method/](https://www.geeksforgeeks.org/collect-js-tojson-method/)

**toJson()方法**用于将集合转换为 Json 字符串。 **JSON** 或**J**ava**S**script**O**object**N**旋转是一种用于结构化数据的格式，web 应用程序使用该格式来相互通信。

**语法:**

```
collect.toJson()
```

**参数:**collect()方法接受一个转换为集合的参数，然后对其应用 toJson()方法。

**返回值:**这个方法返回一个 JSON 字符串。

下面的例子说明了 collect.js 中的 toJson()方法:

**例 1:**

## java 描述语言

```
const collect = require('collect.js'); 

let obj = [
    { 
        username: 'code_hunt',
        user_id: 123456,
        organisation: 'geeksforgeeks',
    } 
];

const collection = collect(obj);   

const newObject = collection.toJson(); 

console.log(newObject);
```

**输出:**

```
{
    "username": "code_hunt", 
    "user_id": 123456, 
    "organisation": "geeksforgeeks"
}
```

**例 2:**

## java 描述语言

```
const collect = require('collect.js'); 

let obj = [ 
    { 
        name: 'Rahul', 
        dob: '25-10-96', 
    }, 
    { 
        name: 'Aditya', 
        dob: '23-10-96', 
    } 
]; 

const collection = collect(obj);   

const newObject = collection.toJson(); 

console.log(newObject);
```

**输出:**

```
{"name": "Rahul", "dob": "25-10-96"}, 
{"name": "Aditya", "dob": "23-10-96"}
```