# 如何在 JavaScript 中对一个 URL 进行编码和解码？

> 原文:[https://www . geesforgeks . org/如何对 javascript 中的 url 进行编码和解码/](https://www.geeksforgeeks.org/how-to-encode-and-decode-a-url-in-javascript/)

**对 URI** 和 URI 组件进行编码和解码是 web 开发中的常见任务，同时用查询参数向 API 发出 GET 请求。很多时候用查询参数构造一个 URL 字符串，为了理解它，响应服务器需要解码这个 URL。浏览器会自动对网址进行编码，即它会将一些特殊字符转换为其他保留字符，然后发出请求。例如:空格字符“”被转换为+或%20。

**示例:**

*   打开 www.google.com，写一个搜索查询“极客对极客”。
*   搜索结果出现后，观察浏览器的网址栏。浏览器网址将由%20 或+号代替空格组成。
*   网址将显示为:https://www.google.com/search?q=geeks%20for%20geeks 或 https://www.google.com/search?q=geeks+for+geeks

**注**:浏览器自动将空格转换为+号或%20 号。

还有许多其他特殊字符，通过硬编码来转换每一个字符将是乏味的。Javascript 提供以下功能来执行此任务:
**编码 URL:** 用 JavaScript 编码可以通过以下方式实现

*   encodeURI 函数
*   逃避()

**1。encodeURI 函数:**encodeURI()函数用于编码完整的 URI。该函数对除(，/？:@ & = + $ #)个字符。

**语法:**

```
encodeURI( complete_uri_string )
```

**参数**:该函数接受一个参数 complete_uri_string，用于保存要编码的网址。

**返回值:**这个函数返回编码的 URI。

## java 描述语言

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

**encodeURIComponent():**encodeURIComponent()函数用于对 URI 的某些部分或组件进行编码。该函数对特殊字符进行编码。此外，它还对以下字符进行编码:，/？:@ & = + $ #

**语法:**

```
encodeURIComponent( uri_string_component )
```

**参数:**该函数接受单参数 uri_string_component，用于保存需要编码的字符串。

**返回值:**该函数返回编码后的字符串。

## java 描述语言

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

【encodeURIComponenet 和 encodeURI:

<figure class="table">

|  | **编码器元件** | 编码 |
| **定义** | The encodeURIComponent () function is used to encode some parts or components of URI. | The encori () function is used to encode the complete URI. |
| **Grammar** | encodeURIComponent(uri _ string _ component) | encodeURI(完整 _ uri _ string) |
| **Special character code** | This function encodes special characters. In addition, it encodes the following characters:,/? :@ & = + $ # | This function divides by (,/? : @&=+$ #) characters. |

</figure>

**2。** **escape()函数:**该函数将字符串作为单个参数&对可以通过支持 ASCII 字符的计算机网络传输的字符串进行编码。编码是将纯文本转换为密文的过程。

**语法:**

```
escape( string )
```

**参数:**该函数接受单个参数:

**返回值:**返回编码字符串。

**注意:**escape()函数只对特殊字符进行编码，此函数不推荐使用。

**异常:**@–+。/ * _

## java 描述语言

```
<script>
const url = "https://www.google.com/search?q=geeks for geeks";
const encodedURL = encodeURI(url);// encoding using encodeURI
document.write(encodedURL)
document.write("<br>"+escape(url)); //encoding using escape

</script>
```

**输出:**

```
https://www.google.com/search?q=geeks%20for%20geeks
https%3A//www.google.com/search%3Fq%3Dgeeks%20for%20geeks
```

**解码网址:**用 Javascript 解码可以通过以下方式实现

*   decodeURI()函数。
*   unescape()函数。

**1。decodeURI 函数:**decodeURI()函数用于解码 encodeURI()生成的 URI。

**语法:**

```
decodeURI( complete_encoded_uri_string )
```

**参数:**这个函数接受一个保存编码字符串的参数 complete_encoded_uri_string。

**返回值:**该函数返回解码后的字符串(原始字符串)。

**例**:

## java 描述语言

```
<script>
const url = "https://www.google.com/search?q=geeks%20for%20geeks";
const decodedURL = decodeURI(url);
document.write(decodedURL)
</script>
```