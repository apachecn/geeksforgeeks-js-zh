# 如何检查给定的字符串是 JavaScript 中另一个字符串的字谜？

> 原文:[https://www . geesforgeks . org/如何检查给定字符串是 javascript 中另一个字符串的字谜/](https://www.geeksforgeeks.org/how-to-check-a-given-string-is-an-anagram-of-another-string-in-javascript/)

**字谜:**字谜是一个单词或句子，通常包含所有原始字母恰好一次，以便排列不同术语或短语的字母。一些例子如下:

> **1。邪恶=卑鄙**
> 
> **2。绅士=优雅的男人**
> 
> **3。十一加二=十二加一**

**示例 1:** 使用内置功能。

## 超文本标记语言

```
<script>
    function checkAnagram(a, b) {

        // Not of same length, can't be Anagram
        if (a.length !== b.length) {
            return false;
        }

        // Inbuilt functions to rearrange the string
        var str1 = a.split('').sort().join(''); 
        var str2 = b.split('').sort().join('');

        var result = (str1 === str2);
        return result;
    }

    // Checking the output
    document.write(checkAnagram('abc', 'cba'));
</script>
```

**输出:**

```
true
```

**例 2** :不使用内置功能。

## 超文本标记语言

```
<script>
    function checkAnagram(a, b) {
        var array = {};
        if (a === b) {
            return true;
        }
        if (a.length !== b.length) {
            return false;
        }
        for (let i = 0; i < a.length; i++) {
            let res = a.charCodeAt(i) - 97;
            array[res] = (array[res] || 0) + 1;
        }

        for (let j = 0; j < b.length; j++) {
            let res = b.charCodeAt(j) - 97;
            if (!array[res]) {
                return false;
            }
            array[res]--;
        }
        return true;
    }
    document.write(checkAnagram('abc', 'cba'));
</script>
```

**输出:**

```
true
```