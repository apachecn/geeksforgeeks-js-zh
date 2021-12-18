# 如何将一个 JavaScript 迭代器转换成数组？

> 原文:[https://www . geeksforgeeks . org/如何将 javascript 迭代器转换为数组/](https://www.geeksforgeeks.org/how-to-transform-a-javascript-iterator-into-an-array/)

任务是将迭代器转换成数组

这可以通过迭代迭代器的每个值并将该值存储到另一个数组中来实现

**方法:**

要为数组创建迭代器:

```
const it = array[Symbol.iterator](); 
```

所以首先我们为名为“它”的“数组”做一个迭代器。创建迭代器后，我们迭代存储在该迭代器中的每个值，并使用下面的代码

```
p.push(word) 
```

将其推入另一个名为“p”的数组中

其中单词是对应于迭代器中存储的数组元素的值。迭代完每个元素后，我们得到最终的数组，迭代器的所有值都存储在 p 中。

**例:**

## JavaScript

```
<script>
    const array = ['Geeks', 'for', 'Geeks'];
    p=[]
    const it = array[Symbol.iterator]();
    document.write(it);
    document.write("<br>");

    for(let word of it)
    {
       p.push(word)
    }
document.write(
"After the conversion the array becomes");
document.write("<br>");
document.write(p);
</script>
```

输出:

```
[object Array Iterator]
After the conversion the array becomes
["Geeks", "for", "Geeks"]
```