# 将 JavaScript 对象展平为单深度对象

> 原文:[https://www . geesforgeks . org/flat-JavaScript-objects-in-single-depth-object/](https://www.geeksforgeeks.org/flatten-javascript-objects-into-a-single-depth-object/)

给定一个嵌套的 JavaScript 对象，任务是展平该对象，并将所有值拉到一个深度。如果这些值已经在单一深度，那么它返回的结果不变。

**typeof()方法:**脚本中使用 typeof()方法检查 JavaScript 变量的类型。

**语法:**

```
typeof(variable)
```

**参数:**该方法接受一个参数，如上所述，如下所述:

*   **变量:**输入变量。

**返回值:**这个方法返回一个包含传递变量类型的字符串。

**进场:**

1.  我们做了一个叫做扁平化对象的函数，它接受一个对象的输入并返回一个对象。
2.  遍历对象并检查当前属性的类型:
    *   如果它属于对象类型，并且不是数组，则再次递归调用该函数。
    *   否则，将该值存储在结果中。
3.  返回对象。

**示例:**

## java 描述语言

```
// Declare an object
let ob = {
    Company: "GeeksforGeeks",
    Address: "Noida",
    contact: +91-999999999,
    mentor: {
        HTML: "GFG",
        CSS: "GFG",
        JavaScript: "GFG"
    }
};

// Declare a flatten function that takes
// object as parameter and returns the
// flatten object
const flattenObj = (ob) => {

    // The object which contains the
    // final result
    let result = {};

    // loop through the object "ob"
    for (const i in ob) {

        // We check the type of the i using
        // typeof() function and recursively
        // call the function again
        if ((typeof ob[i]) === 'object' && !Array.isArray(ob[i])) {
            const temp = flattenObj(ob[i]);
            for (const j in temp) {

                // Store temp in result
                result[i + '.' + j] = temp[j];
            }
        }

        // Else store ob[i] in result directly
        else {
            result[i] = ob[i];
        }
    }
    return result;
};

console.log(flattenObj(ob));
```

**输出:**

```
{
  Company: 'GeeksforGeeks',
  Address: 'Noida',
  contact: -999999908,
  'mentor.HTML': 'GFG',
  'mentor.CSS': 'GFG',
  'mentor.JavaScript': 'GFG'
}
```