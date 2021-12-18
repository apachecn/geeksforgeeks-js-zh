# 如何用 JavaScript 解析 URL？

> 原文:[https://www . geesforgeks . org/如何使用 javascript 解析 URL/](https://www.geeksforgeeks.org/how-to-parse-url-using-javascript/)

给定一个网址，任务是解析该网址，并使用 JavaScript 检索所有相关数据。

**示例:**

```
URL: https://www.geeksforgeeks.org/courses
When we parse the above URL then we can find
hostname: geeksforgeeks.com
path: /courses

```

**方法 1:** 在这个方法中，我们将使用 [createElement()方法](https://www.geeksforgeeks.org/html-dom-createelement-method/)创建一个 HTML 元素，锚定标签，然后使用它来解析给定的 URL。

```
<script>

// Store the URL into variable
var url = "https://geeksforgeeks.org/pathname/?search=query";

// Created a parser using createElement() method
var parser = document.createElement("a");
parser.href = url;

// Host of the URL
document.write(parser.host + "<br>");

// Hostname of the URL
document.write(parser.hostname + "<br>");

// Pathname of URL
document.write(parser.pathname + "<br>");

// Search in the URL
document.write(parser.search + "<br>");

</script>
```

**输出:**

```
geeksforgeeks.org
geeksforgeeks.org
/pathname/
?search=query

```

**方法 2:** 在这个方法中，我们将使用 URL()创建一个新的 URL 对象，然后使用它来解析提供的 URL。

```
<script>

// Store the URL into variable
var url = 
"https://geeksforgeeks.org:3000/pathname/?search=query";

// Created a URL object using URL() method
var parser = new URL(url);

// Protocol used in URL
document.write(parser.protocol + "<br>");

// Host of the URL
document.write(parser.host + "<br>");

// Port in the URL
document.write(parser.port + "<br>");

// Hostname of the URL
document.write(parser.hostname + "<br>");

// Search in the URL
document.write(parser.search + "<br>");

// Search parameter in the URL
document.write(parser.searchParams + "<br>");

</script>
```

**输出:**

```
https:
geeksforgeeks.org:3000
3000
geeksforgeeks.org
?search=query
search=query

```