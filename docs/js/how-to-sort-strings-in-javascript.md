# JavaScript 中字符串如何排序？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中对字符串进行排序/](https://www.geeksforgeeks.org/how-to-sort-strings-in-javascript/)

我们可以通过下面描述的方法对 JavaScript 中的字符串进行排序:

*   **使用 sort()方法**
*   **使用循环**

**使用 sort()方法:**在该方法中，我们使用 JavaScript 的预定义 [sort()](https://www.geeksforgeeks.org/javascript-array-sort/) 方法对字符串数组进行排序。此方法仅在字符串为字母时使用。如果我们将数字存储在数组中并应用这种方法，将会产生错误的结果。

**示例:**

> **原弦**
> 苏拉吉、桑吉夫、拉金什、雅什、拉维
> T4【整理后
> 拉金什、拉维、桑吉夫、苏拉吉、雅什
> 
> **原弦**
> 40、100、1、5、25、10
> **整理后**
> 1、10、100、25、40、5

下面的程序说明了上述方法:

**程序:**

```
<script>
// JavaScript code to sort strings

// Original string
var string = ["Suraj", "Sanjeev", "Rajnish", "Yash", "Ravi"];

// Print original string array
document.write("Original String</br>");
document.write(string);

document.write("</br>");

// Use sort() method to sort the strings
string.sort();

document.write("</br>After sorting</br>");

// Print sorted string array
document.write(string);

</script>                    
```

**输出:**

```
Original String
Suraj, Sanjeev, Rajnish, Yash, Ravi

After sorting
Rajnish, Ravi, Sanjeev, Suraj, Yash

```

**使用循环:**我们将使用一种简单的排序方法来对字符串进行排序。在这个方法中，我们将使用一个循环，然后比较每个元素，并将字符串放在正确的位置。在这里，我们可以将数字存储在数组中，并应用此方法对数组进行排序。
**例:**

> **原弦**
> 苏拉吉、桑吉夫、拉金什、雅什、拉维
> T4【整理后
> 拉金什、拉维、桑吉夫、苏拉吉、雅什
> 
> **原弦**
> 40，100，1，5，25，10
> **整理后**
> 1，5，10，25，40，100

下面的程序说明了上述方法:

**程序:**

```
<script>
// JavaScript code to sort the strings

// Function to perform sort
function string_sort(str) {
    var i = 0, j;
    while (i < str.length) {
        j = i + 1;
        while (j < str.length) {
            if (str[j] < str[i]) {
                var temp = str[i];
                str[i] = str[j];
                str[j] = temp;
            }
            j++;
        }
        i++;
    }
}

// Driver code

// Original string
var string = ["Suraj", "Sanjeev", "Rajnish", "Yash", "Ravi"];

// Print original string array
document.write("Original String</br>");
document.write(string);

document.write("</br>");

// Call string_sort method
string_sort(string);

document.write("</br>After sorting</br>");

// Print sorted string array
document.write(string);

</script>                                  
```

**输出:**

```
Original String
Suraj, Sanjeev, Rajnish, Yash, Ravi

After sorting
Rajnish, Ravi, Sanjeev, Suraj, Yash

```