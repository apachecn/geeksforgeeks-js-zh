# 检查两个给定的字符串在 JavaScript 中是否同构

> 原文:[https://www . geesforgeks . org/check-两个给定字符串在 javascript 中是同构的/](https://www.geeksforgeeks.org/check-two-given-strings-are-isomorphic-in-javascript/)

如果可以将第一个字符串的每个字符映射到第二个字符串的每个字符，那么这两个字符串就被称为同构。基本上，在同构字符串中，第一个字符串的每个字符与第二个字符串的每个字符之间存在一对一的映射。

**例 1:**

```
str1 = 'ABCA'
str2 = 'XYZX'
'A' maps to 'X'
'B' maps to 'Y'
'C' maps to 'Z'
```

这里，第一个字符串的每个字符到第二个字符串的每个字符之间的映射是可能的。所以 str1 和 str2 是同构的。

**例 2:**

```
str1 = 'ABCA'
str2 = 'WXYZ'
'A' maps to 'W'
'B' maps to 'X'
'C' maps to 'Y'
'A' again maps to 'Z'
```

这两个字符串不是同构的，因为第一个字符串中的字符“A”与第二个字符串中的两个字符映射在一起。

**检查同构字符串的一种可能方法是，我们是否可以用一个字符替换第一个字符串的每个字符，以获得第二个字符串，反之亦然。**

**方法:**要检查字符串是否同构，我们必须注意以下条件:

*   两个字符串的长度应该相等
*   两个字符串的当前字符不应该已经映射到其他字符。

我们将使用一个**散列表**来存储从 **str1** 到 **str2 的字符之间的映射。**我们还将使用**设置**来存储 **str2 的已映射字符。**

下面是上述方法的实现。

## java 描述语言

```
<script>
    // JavaScript program for above approach

    // Function to check isomorphic strings
    function isIsomorphic(str1, str2) {

        // If length of strings are not equal then 
        // they are not isomorphic
        if (str1.length !== str2.length) {
            return false;
        }

        // Map to store the mapping between 
        // characters of first string to second
        const map = new Map();

        // Set to store the already mapped
        // character of second string
        const set = new Set();

        for (let i = 0; i < str1.length; i++) {

            // Taking ith char from both strings
            char1 = str1.charAt(i);
            char2 = str2.charAt(i);

            // If char1 has already been mapped
            if (map.has(char1) == true) {

                // Then we have to check that 
                // mapped char should be same
                if (map.get(char1) !== char2) {
                    return false;
                }
            }

            // If char1 is appearing for the first time
            else {

                // Check in the set that the char2
                // is already there or not
                if (set.has(char2)) {
                    return false;
                }

                // If none of above condition is true
                // it means both char1 and char2 are 
                // appearing for the first time
                // insert thm into the map
                map.set(char1, char2);
                set.add(char2);
            }
        }
        return true;
    }
    str1 = "ABCA";
    str2 = "XYZX";
    document.write(isIsomorphic(str1, str2));
</script>
```

**输出:**

```
true
```