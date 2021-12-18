# JavaScript symbol . asynciterrator 属性

> 原文:[https://www . geeksforgeeks . org/JavaScript-symbol-asynciterrator-property/](https://www.geeksforgeeks.org/javascript-symbol-asynciterator-property/)

**符号异步计数器**属性用于将对象设置为异步可迭代对象。这个对象的可迭代属性可以使用循环的**来迭代。**

异步可迭代对象是返回一个函数的任何对象，该函数为它的 Symbol.asyncIterator 属性产生一个 AsyncIterator。

**符号. asyncIterator】符号是一个内置符号，用于访问对象的@ @ asyncIterator 方法。**

**注意:**要使一个对象成为异步可迭代对象，它必须有一个 Symbol.asyncIterator 键。

<figure class="table">

| 符号的属性 |
| --- |
| 可写的 | 不 |
| 可列举的 | 不 |
| 可配置的 | 不 |

</figure>

上述属性的示例代码如下:

**例 1:**

## java 描述语言

```
<script>
    // JavaScript program to demonstrate
    // the Symbol.asyncIterator Property

    // Defining an async iterable 
    const GFG = {

        // Setting the [Symbol.asyncIterator] 
        // property on the object
        async*[Symbol.asyncIterator]() {

            // Using yield keyword to pause
            // and resume generator function
            let i = 0;
            while (i < 10) {
                if (i % 3 == 0) {
                    yield i;
                }
                i++;
            }
        }

    };

    (async () => {

        // Iterate over the async iterable
        // object i.e. myAsyncIterable
        // using for await... loop
        for await (const x of GFG) {
            document.write(x + "<br>");
        }
    })();

</script>
```

**输出:**

```
0
3
6
9
```

**例 2:**

## java 描述语言

```
<script>
    // JavaScript program to demonstrate
    // the Symbol.asyncIterator Property

    // Defining an async iterable 
    const myAsyncIterable = {

        // Setting the [Symbol.asyncIterator] 
        // property on the object
        async*[Symbol.asyncIterator]() {

            let i = 0;
            while (i < 5) {

                // Using yield keyword to 
                // yield values of i
                yield i++;
            }
        }
    };

    (async () => {

        // Iterate over the async iterable
        // object i.e. myAsyncIterable
        // using for await... loop
        for await (const num of myAsyncIterable) {
            document.write(num + "<br>");
        }
    })();

</script>
```

**输出**

```
0
1
2
3
4
```

**浏览器支持:**JavaScript symbol . asynnciterator 属性支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   边缘
*   歌剧
*   旅行队