# 使用 JavaScript 显示文档中存在的链接数量

> 原文:[https://www . geesforgeks . org/display-number-link-present-document-use-JavaScript/](https://www.geeksforgeeks.org/display-number-links-present-document-using-javascript/)

浏览器中加载的任何网页都可以由文档界面表示。这是 DOM 树的入口点，DOM 树包含所有元素，如、<title>、<table>、<a>等。</a></table></title>

我们可以使用 Document()构造函数创建一个 Document 对象。这些文档对象有许多属性。这样的属性之一就是 ***链接*** 。links 属性为我们提供了文档中所有<区域>元素和< a >元素的集合。还有一个属性是*长度*属性。length 属性告诉我们*文档中存在的链接数。因此， *document.links.length* 语句给出了文档中存在的链接数量。*

在 HTML 文档下面包含一段 JavaScript 代码，它告诉我们文档中存在的链接数量:

```
<!DOCTYPE html>
<html>
<body>

<a href = "www.geeksforgeeks.org"></a>
<a href="practice.geeksforgeeks.org"></a>

<script type="text/javascript">
  document.write("Number of links: " + 
                  document.links.length);
</script>

</body>
</html>
```

输出:

```
2

```