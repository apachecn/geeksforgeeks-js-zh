# 如何在 JavaScript 中获取以字节为单位的字符串长度？

> 原文:[https://www . geesforgeks . org/如何获取 javascript 中的字节字符串长度/](https://www.geeksforgeeks.org/how-to-get-the-length-of-a-string-in-bytes-in-javascript/)

**任务:**以字节为单位查找给定字符串的大小。

**示例:**

```
Input: "GeeksForGeeks"
Output: 13 bytes

Input: 20€
Output: 5 bytes

Input: "????"
Output: 4 bytes
```

为了实现这一点，我们有两种方法第一种是使用 Blob API，第二种是 Buffer API，第一种适用于浏览器，第二种适用于 Node.js 环境。 [blob](https://www.geeksforgeeks.org/javascript-blob/) 对象只是一组保存文件中存储的数据的字节。为了使用 blog 读取字符串的字节，我们创建一个 Blob 对象的新实例，然后在其中传递字符串，通过使用 size 属性，我们可以获得字符串的字节。

**示例 1:** 使用 Blob API。

## java 描述语言

```
<script>
const len = (str) => {

  // Creating new Blob object and passing string into it 
  // inside square brackets and then 
  // by using size property storin the size 
  // inside the size variable
  let size = new Blob([str]).size;
  return size;
} 

console.log(len("Geeksforgeeks"))
console.log(len("true"))
console.log(len("false"))
console.log(len("12345"))
console.log(len("20€"))
console.log(len("????"))
</script>
```

**输出:**

```
13
4
5
5
5
4
```

**例 2:** 使用缓冲 API。现在有另一种方法可以在 NodeJS 中使用 Buffer 实现这一点。因此，首先创建 Buffer 对象，然后在其中传递字符串，并使用 length 属性获得字符串的大小

## java 描述语言

```
<script>
const len = (str) => {
  let size = Buffer.from(str).length;
  return size;
} 

console.log(len("Geeksforgeeks"))
console.log(len("true"))
console.log(len("false"))
console.log(len("12345"))
console.log(len("20€"))
console.log(len("????"))
</script>
```

**输出:**

```
13
4
5
5
5
4
```