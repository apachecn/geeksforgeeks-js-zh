# JavaScript 数学 atanh()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-atanh-method/](https://www.geeksforgeeks.org/javascript-math-atanh-method/)

下面是**数学方法的例子。** 

*   **例:**

## 超文本标记语言

```
<script type="text/javascript">
       document.write("When 1 is passed as a parameter: "
                     + Math.atanh(1));
</script>
```

*   **输出:**

```
When 1 is passed as a parameter: Infinity
```

**Math.atanh()** 方法用于返回一个数的双曲反正切。atanh()是 Math 的静态方法，因此它总是用作 Math.atanh()，而不是创建的 Math 对象的方法。

> Math.atanh (x) = arctanh(x) = y，这样 tanh (y) = x

**语法:**

```
Math.atanh(value)
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **值:**此参数保存你想知道其双曲反正切的数字。

**返回:**返回给定数字的双曲反正切。
下面的例子说明了 JavaScript 中的 Math atanh()方法

*   **例 1:**

```
Input : Math.atanh(1)
Output : Infinity
```

*   **例 2:**

```
Input : Math.atanh(0)
Output : 0
```

*   **例 3:**

```
Input : Math.atanh(2)
Output : NaN
```

*   **例 4:**

```
Input : Math.atanh(0.5)
Output : 0.5493061443340548
```

以上方法的更多示例代码如下:
**程序 1:**

## 超文本标记语言

```
<script type="text/javascript">
       document.write("When 0 is passed as a parameter: "
       + Math.atanh(0));
</script>
```

**输出:**

```
When 0 is passed as a parameter: 0
```

**节目 2:**

## 超文本标记语言

```
<script type="text/javascript">
        document.write("When 2 is passed as a parameter: "
        + Math.atanh(2));
</script>
```

**输出:**

```
When 2 is passed as a parameter: NaN
```

**节目 3:**

## 超文本标记语言

```
<script type="text/javascript">
        document.write("When 0.5 is passed as a parameter: "
        + Math.atanh(0.5));
</script>
```

**输出:**

```
When 0.5 is passed as a parameter: 0.5493061443340548
```

**支持的浏览器:**

*   谷歌 Chrome 38.0
*   Internet Explorer 12.0
*   Firefox 25.0
*   Opera 25.0
*   Safari 8.0