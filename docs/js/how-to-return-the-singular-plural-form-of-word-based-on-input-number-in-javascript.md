# 如何在 JavaScript 中根据输入的数字返回单词的单数/复数形式？

> 原文:[https://www . geesforgeks . org/如何根据 javascript 中的输入数字返回单词的单复数形式/](https://www.geeksforgeeks.org/how-to-return-the-singular-plural-form-of-word-based-on-input-number-in-javascript/)

在本文中，我们将学习如何根据输入的数字返回单词的单数或复数形式。这可用于需要根据值动态更改单词的情况。这可以通过两种方法来实现。

**方法 1:** 将单词的单数和复数形式传递给函数。在这种方法中，可以创建一个简单的函数，该函数接收单词的单数和复数形式以及计数值，并根据计数返回适当的单词。我们可以使用三元运算符(？)来检查所需的计数。

**语法:**

```html
function pluralizeWord(singularWord, pluralWord, count) {
  return count > 1 ? pluralWord : singularWord;
}
```

**例 1:**

## 超文本标记语言

```html
<html>
<body>
  <h1 style="color: green;">
    GeeksforGeeks
  </h1>
  <b>
    How to return the singular or plural
    form of the word based on the input
    number in JavaScript?
  </b>
  <script>

    function pluralizeWord(singularWord, pluralWord, count) {
      return count > 1 ? pluralWord : singularWord;
    }

    console.log(1, pluralizeWord("geek", "geeks", 1));
    console.log(4, pluralizeWord("geek", "geeks", 4));
    console.log(4, pluralizeWord("spy", "spies", 4));
    console.log(1, pluralizeWord("man", "men", 1));
    console.log(4, pluralizeWord("man", "men", 4));
  </script>
</body>
</html>
```

**输出:**

```html
1 "geek"
4 "geeks"
4 "spies"
1 "man"
4 "men"
```

**方法 2:** 创建单词所有可能复数形式的词典。如果代码中重复出现大量单词，上述方法效率低下。我们可以通过创建一个单词复数值的字典来解决这个问题，并在检查计数后使用这个字典来选择合适的单词。

**语法:**

```html
let pluralDict = {
      "geek": "geeks",
      "spy": "spies",
      "foot": "feet",
      "woman": "women"
    }

function pluralizeWord(singularWord, count) {
  return count > 1 ? pluralDict[singularWord] : singularWord;
}
```

**例 2:**

## 超文本标记语言

```html
<html>
<body>
  <h1 style="color: green;">
    GeeksforGeeks
  </h1>
  <b>
    How to return the singular or plural
    form of the word based on the input 
    number in JavaScript?
  </b>
  <script>

    // Define the dictionary with the
    // key-value pairs as the singular
    // and plural versions of the word
    let pluralDict = {
      "geek": "geeks",
      "spy": "spies",
      "foot": "feet",
      "woman": "women"
    }

    function pluralizeWord(singularWord, count) {
      return count > 1 ?
        pluralDict[singularWord] : singularWord;
    }

    console.log(4, pluralizeWord("geek", 4));
    console.log(1, pluralizeWord("geek", 1));
    console.log(4, pluralizeWord("spy", 4));
    console.log(1, pluralizeWord("woman", 1));
    console.log(4, pluralizeWord("foot", 4));
  </script>
</body>
</html>
```

**输出:**

```html
 4 "geeks"
 1 "geek"
 4 "spies"
 1 "woman"
 4 "feet"
```