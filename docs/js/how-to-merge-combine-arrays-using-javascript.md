# 如何使用 JavaScript 合并/组合数组？

> 原文:[https://www . geeksforgeeks . org/如何使用 javascript 合并-组合-数组/](https://www.geeksforgeeks.org/how-to-merge-combine-arrays-using-javascript/)

JavaScript 中有很多合并数组的方法。我们将讨论在合并数组时经常遇到的两个问题陈述:

1.  合并而不删除重复的元素。
2.  删除重复元素后合并。

**合并而不删除重复元素:**我们首先从三个数组开始合并。稍后，我们将把它推广到不定数量的数组。

这三个阵列陈述如下:
`let nums1 = [1, 2, 3, 4]`
`let nums2 = [3, 4, 5, 6]`
`let nums3 = [5, 6, 7, 8]`

我们必须合并它们，这样我们的新阵列就变成:

```
combinedNums = [1, 2, 3, 4, 3, 4, 5, 6, 5, 6, 7, 8]
```

1.  **Using [concat() Method](https://www.geeksforgeeks.org/javascript-array-prototype-concat-function/):** The concat() method accept arrays as arguments and returns the merged array.

    ```
    <script>

        // Elements of nums2 and nums3 concatenated
        // with elements of nums1 and returns the 
        // combined array - combinedSum array
        let combinedNums = nums1.concat(nums2, nums3);

        // More readable form
        let combinedNums = [].concat(nums1, nums2, nums3);

        console.log(combinedNums);
    </script>
    ```

    **输出:**

    ```
    [1, 2, 3, 4, 3, 4, 5, 6, 5, 6, 7, 8]
    ```

2.  **Using spread operator:** [Spread operator](https://www.geeksforgeeks.org/javascript-spread-operator/) spreads the value of the array into its constituent elements.

    ```
    <script>
        let combinedNums = [...nums1, ...nums2, ...nums3];

        console.log(combinedNums);
    </script>
    ```

    **输出:**

    ```
    [1, 2, 3, 4, 3, 4, 5, 6, 5, 6, 7, 8]
    ```

3.  **Using [push() Method](https://www.geeksforgeeks.org/javascript-spread-operator/):** The push() method is used with spread operator to pushes the elements of arrays into the existing array. It is especially helpful when we need to append a value to an existing array and need not return a new array.

    **注意:**如果不使用扩展运算符，则数组作为一个整体被追加。

    ```
    <script>
        nums1.push(...nums2, ...nums3);
        console.log(nums1);

        // If spread operator is not used
        nums1.push(nums2, nums3);
        console.log(nums1);
    </script>
    ```

    **输出:**

    ```
    first log: [1, 2, 3, 4, 3, 4, 5, 6, 5, 6, 7, 8]
    second log: [1, 2, 3, 4, [3, 4, 5, 6], [5, 6, 7, 8]]

    ```

我们现在将**推广**这一点，用于合并不定数量的数组:
我们的函数`mergeArrays`接受任意数量的数组作为参数( [rest](https://www.geeksforgeeks.org/javascript-rest-operator/) 运算符)。我们将使用 [forEach](https://www.geeksforgeeks.org/javascript-array-foreach/) 循环遍历每个数组，并将其添加到我们的最终数组:`mergedArray`中。

下面是使用 concat、spread 运算符和 push 方法的实现:

1.  **使用 [array.concat()方法](https://www.geeksforgeeks.org/javascript-array-concat-method/) :**

```
<script>
    let nums1 = [1, 2, 3, 4];
    let nums2 = [3, 4, 5, 6];

    function mergeArrays(...arrays) {
        let mergedArray = [];

        arrays.forEach(array => {
            mergedArray = mergedArray.concat(array)
        });

        return mergedArray;
    }

    console.log(mergeArrays(nums1, nums2));
</script>
```

**输出:**

```
[1, 2, 3, 4, 3, 4, 5, 6]
```

*   **Using [spread operator](https://www.geeksforgeeks.org/javascript-spread-operator/):**

    ```
    <script>
        let nums1 = [1, 2, 3, 4];
        let nums2 = [3, 4, 5, 6];

        function mergeArrays(...arrays) {
            let mergedArray = [];

            arrays.forEach(array => {
                mergedArray = [...mergedArray, ...array]
            });

            return mergedArray;
        }

        console.log(mergeArrays(nums1, nums2));
    </script>
    ```

    **输出:**

    ```
    [1, 2, 3, 4, 3, 4, 5, 6]
    ```

    *   **Using [Array.push() Method](https://www.geeksforgeeks.org/javascript-array-push-method/):**

    ```
    <script>
        let nums1 = [1, 2, 3, 4];
        let nums2 = [3, 4, 5, 6];

        function mergeArrays(...arrays) {
            let mergedArray = [];

            arrays.forEach(array => {
                mergedArray.push(...array)
            });

            return mergedArray;
        }

        console.log(mergeArrays(nums1, nums2));
    </script>
    ```

    **输出:**

    ```
    [1, 2, 3, 4, 3, 4, 5, 6]
    ```

    **合并和移除重复元素:**考虑以下三种方法:

    1.  **Using [set() method](https://www.geeksforgeeks.org/sets-in-javascript/):** Here, we spread the mergedArray elements into our set. Set stores unique items and removes duplicates. We then spread elements in the set into a new array and return that array having merged non-duplicate elements.

        ```
        <script>
            let nums1 = [1, 2, 3, 4];
            let nums2 = [3, 4, 5, 6];
            let nums3 = [5, 6, 7, 8];

            function mergeNoDuplicates(...arrays) {
                let mergedArray = [];

                arrays.forEach(array => {
                    mergedArray = [...mergedArray, ...array]
                });

                return [...new Set([...mergedArray])];
            }

            console.log(mergeNoDuplicates(nums1, nums2, nums3));
        </script>
        ```

        **输出:**

        ```
        [1, 2, 3, 4, 5, 6, 7, 8]
        ```

    2.  **Using [filter() Method](https://www.geeksforgeeks.org/javascript-array-filter/):** In this approach, we filter out elements of the mergedArray on the basis of their first occurrence in the array. We check whether the item occurs first by taking it’s first index with the help of [indexOf](https://www.geeksforgeeks.org/javascript-array-indexof/) method.

        ```
        <script>
            let nums1 = [1, 2, 3, 4];
            let nums2 = [3, 4, 5, 6];
            let nums3 = [5, 6, 7, 8];

            function mergeNoDuplicates(...arrays) {
                let mergedArray = [];

                arrays.forEach(array => {
                    mergedArray = [...mergedArray, ...array]
                });

                const mergedUnique = mergedArray
                    .filter((item, index) => 
                        mergedArray.indexOf(item) === index);
                return mergedUnique;
            }

            console.log(mergeNoDuplicates(nums1, nums2, nums3));
        </script>
        ```

        **输出:**

        ```
        [1, 2, 3, 4, 5, 6, 7, 8]
        ```

    3.  Using [Array reduce() Method](https://www.geeksforgeeks.org/javascript-array-reduce-method/): In this approach, we take noDuplicates array as our accumulator. An item is appended in this array if it is not already present in the noDuplicates array. If an item is already present, we simply return the current array for the next iteration.

        ```
        <script>
            let nums1 = [1, 2, 3, 4];
            let nums2 = [3, 4, 5, 6];
            let nums3 = [5, 6, 7, 8];

            function mergeNoDuplicates(...arrays) {
                let mergedArray = [];

                arrays.forEach(array => {
                    mergedArray = [...mergedArray, ...array]
                });

                const mergedUnique = mergedArray
                   .reduce((noDuplicates, item) => {
                    if (noDuplicates.includes(item)) {
                        return noDuplicates;
                    }

                    else {
                        return [...noDuplicates, item];
                    }
                }, [])

                return mergedUnique;
            }

            console.log(mergeNoDuplicates(nums1, nums2, nums3));
        </script>
        ```

        **输出:**

        ```
        [1, 2, 3, 4, 5, 6, 7, 8]
        ```