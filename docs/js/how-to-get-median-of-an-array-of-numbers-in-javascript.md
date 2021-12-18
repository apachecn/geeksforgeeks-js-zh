# 如何在 JavaScript 中得到一组数字的中位数？

> 原文:[https://www . geesforgeks . org/如何获取 javascript 中数字数组的中值/](https://www.geeksforgeeks.org/how-to-get-median-of-an-array-of-numbers-in-javascript/)

在本文中，我们将看到如何使用 JavaScript 找到数组的中值。

**示例:**

```
Input arr1 : [1 4 7 9]
Output : 5.5
Explanation : The median of the two sorted array is 
              the middle elements which is 5 if the 
              arrayLength =arr1.length + arr2.length is odd 
              if the array length is even then it will be 
              the average of two number 

Input: arr1 : [5 3 1 8 90]

Output: 5
Explanation : The median is average of two number 
              because the array.length is even for this case.
```

**方法:**这里我们先对数组进行排序，然后会求出数组长度。如果数组长度是偶数，那么中值将是 arr[(arr . length)/2]+arr[((arr . length)/2)+1]。如果数组长度是奇数，那么中间值将是一个中间元素。

## java 描述语言

```
<script>
    function medianof2Arr(arr1) {
        var concat = arr1;
        concat = concat.sort(
            function (a, b) { return a - b });

        console.log(concat);
        var length = concat.length;

        if (length % 2 == 1) {

            // If length is odd
            console.log(concat[(length / 2) - .5])
            return concat[(length / 2) - .5]

        }
        else {
            console.log((concat[length / 2] 
                + concat[(length / 2) - 1]) / 2);

            return (concat[length / 2] 
                + concat[(length / 2) - 1]) / 2;
        }
    }

    arr1 = [1, 4, 7, 9]

    medianof2Arr(arr1)
</script>
```

**输出:**

```
5.5
```

时间复杂性:

```
O(n + m)
```

**方法 2:** 这里我们先做了变量**中间**，不管数组长度是奇数还是偶数，都有中间值。之后，我们通过避免突变对数组进行排序。突变意味着用另一个对象名改变对象名，或者将对象传递给另一个对象，称为突变。

可以用**参考数据**类型来完成，这些类型是**数组、**T4】对象所以现在避免这个。之后，如果数组的长度是偶数，那么我们在数组中的位置 arr 处有两个值((arr . length)/2)+arr((arr . length)/2)+1)。然后取这两个数的平均值，作为中位数返回。

## java 描述语言

```
<script>
    function median_of_arr(arr) {
        const middle = (arr.length + 1) / 2;

        // Avoid mutating when sorting
        const sorted = [...arr].sort((a, b) => a - b);
        const isEven = sorted.length % 2 === 0;

        return isEven ? (sorted[middle - 1.5]
            + sorted[middle - 0.5]) / 2 :
            sorted[middle - 1];
    }
    var arr = [1, 4, 7, 9];
    console.log(median_of_arr(arr));

</script>
```

**输出:**

```
5.5
```

**时间复杂度:**

```
O(n+m)
```