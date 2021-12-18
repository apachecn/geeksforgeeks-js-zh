# 如何在 JavaScript 中得到两个数组的对称差？

> 原文:[https://www . geeksforgeeks . org/如何获得 javascript 中两个数组的对称差/](https://www.geeksforgeeks.org/how-to-get-symmetric-difference-between-two-arrays-in-javascript/)

在数学中，两个集合 A 和 B 之间的对称差表示为 AδB =(A–B)∞(B–A)

*   It is defined as the set of all elements that exist in set A or set B but neither exists.
*   Simply put, it is to discard common elements from two sets.

#### 例 1:

```
A = { 1, 2, 3, 4, 5, 6}
B = { 4, 5, 6, 7 }

A - B = { 1, 2, 3, 4, 5, 6} - { 4, 5, 6, 7 }
      = { 1, 2, 3 }
B - A = { 4, 5, 6, 7 } - { 1, 2, 3, 4, 5, 6}
      = { 7, 1, 2, 3 }

A Δ B = ( A - B ) ∪ ( B - A )
      = { 1, 2, 3 } ∪ { 7, 1, 2, 3 }
A Δ B = { 1, 2, 3, 7 }
```

#### 代码:

## java 描述语言

```
<script>
    /* Defining two arrays and a 
                resultant array*/
    const a = [1, 2, 3, 4, 5, 7, 9];
    const b = [5, 6, 7, 8, 9];
    const result = [];

    /* Defining the function with two 
    arguments array inputs */
    function difference(arr1, arr2) {
        var i = 0,
            j = 0;
        var flag = false;

        /* For array 1 */
        for (i = 0; i < arr1.length; i++) {

            /* Reseting the flag and the 
            other array iterator */
            j = 0;
            flag = false
            while (j != arr2.length) {
                if (arr1[i] == arr2[j]) {
                    flag = true;
                    break;
                }
                j++;
            }

            /* If value is not present in the 
            second array then push that value 
            to the resultant array */
            if (!flag) {
                result.push(arr1[i]);
            }
        }
        flag = false;

        /* For array 2 */
        for (i = 0; i < arr2.length; i++) {

            /* Reseting the flag and the 
            other array iterator */
            j = 0;
            flag = false
            while (j != arr1.length) {
                if (arr2[i] == arr1[j]) {
                    flag = true;
                    break;
                }
                j++;
            }

            /* If value is not present in the
            first array then push that value 
            to the resultant array */
            if (!flag) {
                result.push(arr2[i]);
            }
        }
        return result;
    }
    console.log(difference(a, b));
</script>
```

#### 输出:

```
[ 1, 2, 3, 4, 6, 8]
```