# 如何在 Javascript 中查找两个数组是否包含任何公共项？

> 原文:[https://www . geeksforgeeks . org/如何查找两个数组中是否包含任何 javascript 中的公共项/](https://www.geeksforgeeks.org/how-to-find-if-two-arrays-contain-any-common-item-in-javascript/)

给定两个包含数组元素的数组，任务是检查两个数组是否包含任何公共元素，然后返回真，否则返回假。
**例:**

```
Input: array1 = ['a', 'b', 'c', 'd', 'e']
       array2 = ['f', 'g', 'c']
Output: true

Input: array1 = ['x', 'y', 'w', 'z']
       array2 = ['m', 'n', 'k']
Output: false
```

在 JavaScript 中有很多方法可以解决这个问题，下面将讨论其中的一些方法。
**方法一:蛮力进场**

*   将第一个数组中的每一项与第二个数组中的每一项进行比较。
*   循环数组 1，从头到尾迭代一遍。
*   循环数组 2 并从头到尾迭代它。
*   比较数组 1 和数组 2 中的每一项，如果找到任何公共项，则返回 true，否则返回 false。

**例:**

## java 描述语言

```
<script>

// Declare two array
const array1 = ['a', 'b', 'c', 'd'];
const array2 = ['k', 'x', 'z'];

// Function definition with passing two arrays
function findCommonElement(array1, array2) {

    // Loop for array1
    for(let i = 0; i < array1.length; i++) {

        // Loop for array2
        for(let j = 0; j < array2.length; j++) {

            // Compare the element of each and
            // every element from both of the
            // arrays
            if(array1[i] === array2[j]) {

                // Return if common element found
                return true;
            }
        }
    }

    // Return if no common element exist
    return false;
}

document.write(findCommonElement(array1, array2))
</script>                   
```

**输出:**

```
false
```

**时间复杂度:**O(M * N)
T3】方法二:T5】

*   创建一个空对象并遍历第一个数组。
*   检查对象中是否存在第一个数组中的元素。如果它不存在，那么在数组中分配 properties ===元素。
*   遍历第二个数组，检查第二个数组中的元素是否存在于创建的对象上。
*   如果元素存在，则返回真，否则返回假。

**例:**

## java 描述语言

```
<script>

// Declare Two array
const array1 = ['a', 'd', 'm', 'x'];
const array2 = ['p', 'y', 'k'];

// Function call
function findCommonElements2(arr1, arr2) {

    // Create an empty object
    let obj = {};

        // Loop through the first array
        for (let i = 0; i < arr1.length; i++) {

            // Check if element from first array
            // already exist in object or not
            if(!obj[arr1[i]]) {

                // If it doesn't exist assign the
                // properties equals to the
                // elements in the array
                const element = arr1[i];
                obj[element] = true;
            }
        }

        // Loop through the second array
        for (let j = 0; j < arr2.length ; j++) {

        // Check elements from second array exist
        // in the created object or not
        if(obj[arr2[j]]) {
            return true;
        }
    }
    return false;
}

document.write(findCommonElements2(array1, array2))
</script>                   
```

**输出:**

```
false
```

**时间复杂度:**O(M+N)
T3】方法三:T5】

*   使用内置的 ES6 函数 some()迭代第一个数组的每个元素并测试该数组。
*   使用内置函数 includes()和第二个数组来检查第一个数组中是否存在元素。
*   如果元素存在，则返回真，否则返回假

## java 描述语言

```
<script>

// Declare two array
const array1= ['a', 'b', 'x', 'z'];
const array2= ['k', 'x', 'c']

// Iterate through each element in the
// first array and if some of them
// include the elements in the second
// array then return true.
function findCommonElements3(arr1, arr2) {
    return arr1.some(item => arr2.includes(item))
}

document.write(findCommonElements3(array1, array2))
</script>                   
```

**输出:**

```
true
```

JavaScript 最出名的是网页开发，但它也用于各种非浏览器环境。您可以通过以下 [JavaScript 教程](https://www.geeksforgeeks.org/javascript-tutorial/)和 [JavaScript 示例](https://www.geeksforgeeks.org/javascript-examples/)从头开始学习 JavaScript。