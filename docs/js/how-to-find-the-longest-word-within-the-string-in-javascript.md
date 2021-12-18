# 如何在 JavaScript 中找到字符串内最长的单词？

> 原文:[https://www . geesforgeks . org/如何在 javascript 字符串中找到最长的单词/](https://www.geeksforgeeks.org/how-to-find-the-longest-word-within-the-string-in-javascript/)

给定一个字符串，任务是使用 JavaScript 从字符串中找到最大的单词。

**示例:**

```
Input: "This is a demo String find the largest word from it"
Output: "largest"

Input:  "Hello guys this is geeksforgeeks where students learn programming"
Output: "geeksforgeeks"
```

为此，我们使用以下方法:

1.  使用**正则表达式**和**进行..循环**
2.  使用**分割**和**排序**()方法
3.  使用**分裂**和**减少**()的方法

**方法 1:** 使用正则表达式和 for…循环。在这种方法中，我们使用正则表达式通过使用正则表达式**/【a-Za-Z0-9】+/gi**将字符串分割成一个单词数组，然后使用 for 循环迭代该数组并搜索最大的字符串。

**例 1:**

## index.html

```
<script>
// Javascript program to search largest word from a string

function longest(str){
  // Split the string using regex
  str = str.match(/[a-zA-Z0-9]+/gi);
  // Creating a empty string to store largest word
  let largest = "";

  // Creating a for...loop to iterate over the array
  for(let i = 0; i < str.length; i++){
    // If the i'th item is greater than largest string 
    // then overwrite the largest string with the i'th value
    if(str[i].length > largest.length){
      largest = str[i]
    }
  }
  return largest;
}

console.log(longest("Hello guys this is geeksforgeeks where"+
                    " students learn programming"))
</script>
```

**输出:**

```
"geeksforgeeks"
```

**方法 2:** 使用[分裂()](https://www.geeksforgeeks.org/javascript-string-prototype-split-function/)和[排序()](https://www.geeksforgeeks.org/javascript-array-sort-method/)方法。在这种方法中，我们使用 ***String.split()*** 方法分割字符串，并使用***array . sort()*****方法对数组进行排序。**

****例 2:****

## **index.js**

```
<script>
function longest(str){
  // Split the string into array
  str = str.split(" ")
  // Return the first sorted item of the Array
  return str.sort((a, b) => b.length - a.length)[0]
}

console.log(longest("Hello guys this is geeksforgeeks"+
                    " where students learn programming"))
</script>
```

****输出:****

```
"geeksforgeeks"
```

****进场 3 :** 采用[劈()](https://www.geeksforgeeks.org/javascript-string-prototype-split-function/)和[减()](https://www.geeksforgeeks.org/javascript-array-reduce-method/)的方法。在这种方法中，我们使用 String.split()方法分割字符串，并使用 reduce 方法搜索数组中最大的元素，这是您最大的字符串。**

## **index.js**

```
<script>
function longest(str){
  // Split the string into array
  str = str.split(" ");

  // Get the index of largest item of the array
  let index = str.reduce((acc, curr, i)=>{
    if(curr.length > str[acc].length){
      return i
    }
    return acc;
  }, 0)

  return str[index];
}

console.log(longest("Hello guys this is geeksforgeeks"+
                    " where students learn programming"))
</script>
```

****输出:****

```
**"geeksforgeeks"**
```