# Collect.js | get()函数

> 原文:[https://www.geeksforgeeks.org/collect-js-get-function/](https://www.geeksforgeeks.org/collect-js-get-function/)

**get()函数**用于返回出现在特定键上的值。在 JavaScript 中，首先将数组转换为集合，然后将函数应用于集合。

**语法:**

```
data.get('key')
```

**参数:**该函数接受如上所述的单个参数，如下所述:

*   **Key:** This parameter holds the key name that define the value of that key.

    **返回值:**返回所述键的值。

    以下示例说明了 collect.js 中的 **get()函数**:
    **示例 1:** 在本例中，我们取一个集合，然后使用 get()函数，它使用键返回值。

    ```
    // It is used to import collect.js library
    const collect = require('collect.js');

    const collection = collect({
      firstname: 'Jhon',
      lastname: 'Carter',
    });

    console.log(collection.get('firstname'));
    ```

    **输出:**

    ```
    Jhon
    ```

    **例 2:** 如果键值不存在，则返回 null。

    ```
    // It is used to import collect.js library
    const collect = require('collect.js');

    const collection = collect({
      firstname: 'Jhon',
      lastname: 'Carter',
    });

    console.log(collection.get('middlename'));
    ```

    **输出:**

    ```
    null
    ```

    **例 3:**

    ```
    // It is used to import collect.js library
    const collect = require('collect.js');

    const collection = collect(['a', 'b', 'c']);

    console.log(collection.get(2));
    ```

    **输出:**

    ```
    c
    ```

    **参考:**T2】https://collect.js.org/api/get.html