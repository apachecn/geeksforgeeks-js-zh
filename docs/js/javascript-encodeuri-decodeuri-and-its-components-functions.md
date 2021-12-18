# JavaScript | encodeURI()，decodeURI()及其组件功能

> 原文:[https://www . geesforgeks . org/JavaScript-encodeuri-decodeuri-及其组件-函数/](https://www.geeksforgeeks.org/javascript-encodeuri-decodeuri-and-its-components-functions/)

对 URI 和 URI 组件进行编码和解码是 web 开发中的一项常见任务。很多时候用查询参数构造一个 URL 字符串，为了理解它，响应服务器需要解码这个 URL。浏览器会自动对网址进行编码，即它会将一些特殊字符转换为其他保留字符，然后发出请求。例如:空格字符“”被转换为+或%20。

**示例:**

*   打开 www.google.com，写一个搜索查询“极客对极客”。
*   搜索结果出现后，观察浏览器的网址栏。浏览器网址将由%20 或+号代替空格组成。
*   网址将显示为:https://www.google.com/search?q=geeks%20for%20geeks 或 https://www.google.com/search?q=geeks+for+geeks

**注意:**浏览器自动将空格转换为+号或%20 号。

还有许多其他特殊字符，通过硬编码来转换它们将是乏味的。JavaScript 提供以下功能来执行此任务:

编码器()

encodeURI()函数用于编码完整的 URI。该函数对除(，/？:@ & = + $ #)个字符。

**语法:**

```
encodeURI( complete_uri_string )
```

**参数:**该函数接受单个参数 *complete_uri_string* ，用于保存要编码的网址。

**返回值:**这个函数返回编码的 URI。

**示例:**

```
<script>
const url = "https://www.google.com/search?q=geeks for geeks";
const encodedURL = encodeURI(url);
document.write(encodedURL)
</script>
```

**输出:**

```
https://www.google.com/search?q=geeks%20for%20geeks
```

**编码器元件()**

encodeURIComponent()函数用于对 URI 的某些部分或组件进行编码。该函数对特殊字符进行编码。此外，它还对以下字符进行编码:，/？: @ & = + $ #

**语法:**

```
encodeURIComponent( uri_string_component )
```

**参数:**:该函数接受单个参数 *uri_string_component* ，用于保存需要编码的字符串。

**返回值:**该函数返回编码后的字符串。

**示例:**

```
<script>
const component = "geeks for geeks"
const encodedComponent = encodeURIComponent(component);
document.write(encodedComponent)
</script>
```

**输出:**

```
geeks%20for%20geeks
```

**装饰工()**

decodeURI()函数用于解码 encodeURI()生成的 URI。

**语法:**

```
decodeURI( complete_encoded_uri_string )
```

**参数:**该函数接受保存编码字符串的单个参数*complete _ encoded _ uri _ string*。

**返回值:**该函数返回解码后的字符串(原始字符串)。

**示例:**

```
<script>
const url = "https://www.google.com/search?q=geeks%20for%20geeks";
const decodedURL = decodeURI(url);
document.write(decodedURL)
</script>
```

**输出:**

```
https://www.google.com/search?q=geeks for geeks
```

**decodeURIComponent()**

decodeURIComponent()函数用于解码 encodeURIComponent()生成的 URI 的某些部分或组件。

**语法:**

```
decodeURIComponent( encoded_uri_string_component )
```

**参数:**该函数接受保存编码字符串的单个参数*encoded _ uri _ string _ component*。

**返回值:**该函数返回 URI 字符串的解码分量。

**示例:**

```
<script>
const component = "geeks%20for%20geeks"
const decodedComponent = decodeURIComponent(component);
document.write(decodedComponent)                    
</script>
```

**输出:**

```
geeks for geeks
```

**应用:**

*   正确转换提供给应用编程接口的以空格分隔的查询参数。
*   在网页抓取中解码网址的查询参数以提取人类可读的字符串。