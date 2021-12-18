# 洛达什 _。sortedUniq()方法

> 哎哎哎:# t0]https://www . geeksforgeeks . org/LOD ash-_-sorteduniq method/

_。sortedUniq 方法用于返回数组中可以插入元素的最低索引，并保持其排序顺序。还有，这个方法就像 _。uniq，除了它是为排序数组设计和优化的。In _。uniq 仅保留每个元素的第一次出现，结果值的顺序由它们在数组中出现的顺序决定。

**语法:**

```
_.sortedUniq(array)

```

**参数:**该方法只接受一个参数，如上所述，如下所述:

*   **array:** This parameter holds the array to inspect.

    **返回值:**此方法用于返回新的无重复数组。

    **示例 1:** 这里，const _ = require('lodash ')用于将 lodash 库导入文件。

    ## java 描述语言

    ```
    // Requiring the lodash library 
    const _ = require("lodash"); 

    // Original array 
    let y = ([1, 1, 2, 3, 3, 4]);

    // Use of  _.sortedUniq() 
    // method 
    let index =  _.sortedUniq(y, [1, 1, 2]); 

    // Printing the output 
    console.log(index);
    ```

    **输出:**

    ```
    [ 1, 2, 3, 4 ]

    ```

    **例 2:**

    ## java 描述语言

    ```
    // Requiring the lodash library 
    const _ = require("lodash"); 

    // Original array 
    let y = (['p', 'q', 'r', 't', 't', 'u', 's', 't', 't', 'v', 'w']);

    // Use of  _.sortedUniq() 
    // method 
    let index =  _.sortedUniq(y); 

    // Printing the output 
    console.log(index);
    ```

    **输出:**

    ```
    ['p', 'q', 'r', 't', 'u', 's', 't', 'v', 'w']

    ```

    **例 3:**

    ```
    // Requiring the lodash library 
    const _ = require("lodash"); 

    // Original array 
    let y = (['chemistry', 'computer', 'computer', 

    'english', 'geography', 'hindi', 'hindi', 

    'maths', 'physics']);

    // Use of  _.sortedUniq() 
    // method 
    let index =  _.sortedUniq(y); 

    // Printing the output 
    console.log(index);
    ```

    **输出:**

    ```
    ['chemistry', 'computer', 'english', 
    'geography', 'hindi', 'maths', 'physics']

    ```

    **注意:**这在正常的 JavaScript 中不会起作用，因为它需要安装库 lodash。