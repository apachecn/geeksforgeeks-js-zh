# 如何用 JavaScript 对数值数组进行排序？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 对数字数组进行排序/](https://www.geeksforgeeks.org/how-to-sort-numeric-array-using-javascript/)

[JavaScript Array.sort()方法](https://www.geeksforgeeks.org/javascript-array-sort/)用于对数组元素进行就地排序，并返回排序后的数组。该函数以字符串格式对元素进行排序。它对字符串数组有效，但对数字无效。例如:如果数字按字符串排序，那么“75”比“200”大。
**例:**

```
Input          : [12, 25, 31, 23, 75, 81, 100]
Wrong Output   : [100, 12, 23, 25, 31, 75, 81]
Correct Output : [12, 23, 25, 31, 75, 81, 100]
```

**示例:**本示例以字符串格式对数组元素进行排序。

## java 描述语言

```
<script>

// Declare and initialize original array
var marks = [12, 25, 31, 23, 75, 81, 100];

// Print Before Sortring Array
document.write("Original Array</br>");
document.write(marks);

document.write("</br>");

// Call sort function
marks.sort();

document.write("</br>After Sorting in Ascending Order</br>");

// Print Sorted Numeric Array
document.write(marks);

</script>
```

**输出:**

```
Original Array
12,25,31,23,75,81,100

After Sorting in Ascending Order
100,12,23,25,31,75,81
```

**那么，数组元素的个数如何排序呢？**
有两种方法可以对数字数组进行升序排序。

*   使用比较函数
*   通过创建循环

**使用比较函数:**我们可以创建一个返回负值、零值或正值的比较函数。
**语法:**

```
function(a, b){return a - b}
```

*   负值(a > b)= a 将放在 b 之前
*   零值(a == b) = >无变化
*   正值(a < b ) => a 将放在 b 之后

**示例:**本示例使用 compare 函数对数组元素进行升序排序。

## java 描述语言

```
<script>

// Declare and initialize an Array
var marks = [12, 25, 31, 23, 75, 81, 100];

// Print Before sortring array
document.write("Original Array</br>");
document.write(marks);

document.write("</br>");

// Sort elements using compare method
marks.sort(function(a, b){return a - b});

document.write("</br>After sorting in Ascending order</br>");

// Print sorted Numeric array
document.write(marks);

</script>
```

**输出:**

```
Original Array
12,25,31,23,75,81,100

After sorting in Ascending order
12,23,25,31,75,81,100
```

现在，我们希望按照降序对数组进行排序，而不是改变比较函数。
**语法:**

```
function(a, b){return b - a}
```

*   负值(b < a) => a 将放在 b 之后
*   零值(a == b) = >无变化
*   正值(b > a ) => a 将放在 b 之前

**示例:**本示例使用 compare 函数对数组元素进行降序排序。

## java 描述语言

```
<script>

// Declare and initialize an Array
var marks = [12, 25, 31, 23, 75, 81, 100];

// Print Before sortring array
document.write("Original Array</br>");
document.write(marks);

document.write("</br>");

// Sort elements using compare method
marks.sort(function(a, b){return b - a});

document.write("</br>After sorting in Ascending order</br>");

// Print sorted Numeric array
document.write(marks);

</script>
```

**输出:**

```
Original Array
12,25,31,23,75,81,100

After sorting in Ascending order
100,81,75,31,25,23,12
```

**创建循环:**我们也可以使用循环对数组元素进行排序。这里，我们将使用冒泡排序(简单的排序技术)以升序对数组元素进行排序。
**例:**

## java 描述语言

```
<script>

// Sorting function
function Numeric_sort(ar) {

    var i = 0, j;

    while (i < ar.length) {
        j = i + 1;
        while (j < ar.length) {

            if (ar[j] < ar[i]) {
                var temp = ar[i];
                ar[i] = ar[j];
                ar[j] = temp;
            }
            j++;
        }
        i++;
    }
}

// Original Array
var arr = [1, 15, 10, 45, 27, 100];

// Print Before sortring array
document.write("Original Array</br>");
document.write(arr);

document.write("</br>");

// Function call
Numeric_sort(arr);

document.write("</br>Sorted Array</br>");

// Print sorted Numeric array
document.write(arr);

</script>
```

**输出:**

```
Original Array
1,15,10,45,27,100

Sorted Array
1,10,15,27,45,100
```