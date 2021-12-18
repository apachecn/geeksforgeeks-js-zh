# JavaScript 中的模糊搜索

> 原文:[https://www.geeksforgeeks.org/fuzzy-search-in-javascript/](https://www.geeksforgeeks.org/fuzzy-search-in-javascript/)

模糊搜索符合意思，不一定是精确的措辞或特定的短语。它对数据执行与全文搜索相同的操作，以查看可能的拼写错误和近似字符串匹配。它是一个非常强大的工具，可以考虑到你希望看到的短语的上下文。

模糊搜索也被称为近似字符串匹配。它之所以强大，是因为文本数据通常很混乱。例如，速记和缩写文本在各种数据中很常见。此外，从光学字符识别或语音到文本的转换输出往往是混乱或不完善的。因此，我们希望通过尽可能外推最大数量的信息来充分利用我们的数据。

当用于研究和调查时，模糊搜索比精确搜索更强大。模糊搜索在研究不熟悉的、外语的或复杂的术语时非常有用，这些术语的正确拼写似乎并不广为人知。模糊搜索也可用于定位支持不完整或部分不准确识别信息的个人。

**安装包装:**

```
$ npm install --save fuse.js
```

**例:**

## Javascript

```
const Fuse = require('fuse.js')

const people = [
    {
        name: "John",
        city: "New York"
    },
    {
        name: "Steve",
        city: "Seattle"
    },
    {
        name: "Bill",
        city: "Omaha"
    }
]

const fuse = new Fuse(people, {
    keys: ['name', 'city']
})

// Search
const result = fuse.search('jon')

console.log(result)
```

**输出:**

```
[ { item: { name: 'John', city: 'New York' }, refIndex: 0 } ]

```

JavaScript 常见的模糊搜索库有:

*   **列表。js** :https://listjs.com/
*   **保险丝。js** :https://fusejs.io/
*   **模糊-搜索** :https://www。npmjs。com/包/模糊搜索