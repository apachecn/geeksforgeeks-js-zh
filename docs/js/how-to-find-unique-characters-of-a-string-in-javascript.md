# 如何在 JavaScript 中找到字符串的唯一字符？

> 原文:[https://www . geesforgeks . org/如何在 javascript 中查找唯一字符串字符/](https://www.geeksforgeeks.org/how-to-find-unique-characters-of-a-string-in-javascript/)

本文的目的是使用 JavaScript 在字符串中找到唯一的字符。

**示例:**

```
Input:  Geeksforgeeks
Output: Geksforg

Input:  Geeksforgeeks is a great site for computer science
Output: Geksforg Iaticmpun
```

为此，我们有以下方法:

**方法 1:** 这是一种从字符串中寻找唯一字符的天真方法。在这种方法中，我们创建了一个变量名 *uniq* ，并使用 [*对*](https://www.geeksforgeeks.org/javascript-for-loop/) 循环迭代字符串，每次迭代时，我们都检查 *uniq* 是否包含字符。

## java 描述语言

```
<script>
function findUnique(str){
  // The variable that contains the unique values
  let uniq = "";

  for(let i = 0; i < str.length; i++){
    // Checking if the uniq contains the character
    if(uniq.includes(str[i]) === false){
      // If the character not present in uniq
      // Concatenate the character with uniq
      uniq += str[i]
    }
  }
  return uniq;
}

console.log(findUnique("Geeksforgeeks"))
console.log(findUnique("Geeksforgeeks Is a great site for computer science"))
</script>
```

**输出:**

```
"Geksforg"

"Geksforg Iaticmpun"
```

**方法 2:** 在该方法中，我们使用集合数据结构。集合数据结构只包含唯一的值，我们利用了它。因此，要使用*设置*从字符串中提取唯一值，我们遵循以下步骤。

*   使用 [*split()*](https://www.geeksforgeeks.org/javascript-string-prototype-split-function/) 方法将字符串转换为数组。
*   使用[新建集合()](https://www.geeksforgeeks.org/sets-in-javascript/)创建一个集合，并将转换后的数组传递给它。
*   现在使用扩展运算符将集合转换为数组，例如:***[…集合]***
*   **然后[连接那个数组](https://www.geeksforgeeks.org/javascript-array-join-method)做一个字符串。**

## **java 描述语言**

```
<script>
// Javascript program to extract unique characters from a string
function findUnique(str){

  // Split the string to make array
  str = str.split("")

  // Create a set using array
  str = new Set(str);

  // Convert the set into array using spread
  // operator and join it to make string
  str = [...str].join("");

  return str;
}

console.log(findUnique("Geeksforgeeks"))
console.log(findUnique("Geeksforgeeks Is a great site for computer science"))
</script>
```

****输出:****

```
"Geksforg"

"Geksforg Iaticmpun"
```

****方法 3:** 在这种方法中，我们首先使用扩展运算符将字符串转换为数组，例如 **[…str]** ，然后在该数组上应用 [*约简*](https://www.geeksforgeeks.org/javascript-array-reduce-method/) 方法。**

## **java 描述语言**

```
<script>
// Javascript program to extract unique characters from a string
function findUnique(str){
  return [...str].reduce((acc, curr)=>{
    return acc.includes(curr) ?  acc  :  acc + curr;
  }, "")
}

console.log(findUnique("Geeksforgeeks"))
console.log(findUnique("Geeksforgeeks Is a great site for computer science"))
</script>
```

****输出:****

```
"Geksforg"
"Geksforg Iaticmpun"
```