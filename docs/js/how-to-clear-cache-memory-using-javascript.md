# 如何用 JavaScript 清除缓存内存？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 清除缓存内存/](https://www.geeksforgeeks.org/how-to-clear-cache-memory-using-javascript/)

与移动应用不同，网络浏览器不允许清空缓存。虽然我们不能清除客户端浏览器的所有缓存，但是仍然可以通过在 HTML 代码中使用元标签来加载网页而不缓存。

做到这一点的唯一方法是在代码中做一些改变，这些代码表示浏览器不记得最近加载的内存，它只不过是 chache 内存。

以下是解释
**的两个例子注:**以下代码不能按原样运行，也没有输出。它必须添加到已经存在的代码中才能看到输出。

**方法 1:**

```
<meta http-equiv='cache-control' content='no-cache'>
<meta http-equiv='expires' content='0'>
<meta http-equiv='pragma' content='no-cache'>
```

添加这部分 HTML 代码，使得浏览器不记录缓存内存。

**方法 2:**
在脚本标签的文件名后添加一个参数。当文件改变时改变它。

**示例:**
让这成为文件的名称。每次加载此页面时，只需更改脚本的版本。

```
<script src = "filename.js?version = 1.0"></script>
```

下次你加载这个页面的时候应该是这样的。

```
<script src = "newfile.js?version = 1.1"></script>
```

**注:**

*   浏览器的设计方式是保存所有的临时缓存。
*   之所以如此，是因为缓存内存是网站加载更快的主要原因。
*   因此，没有直接的方法可以永久删除它的缓存，除非你的 HTML 代码中的某些编码被改变。
*   实现这一点的其他方法可能很少，但这两种方法是最简单、最有效的方法。