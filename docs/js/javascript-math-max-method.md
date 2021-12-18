# JavaScript 数学 max()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-max-method/](https://www.geeksforgeeks.org/javascript-math-max-method/)

下面是 **Math max()** 方法的例子。

*   **例:**

## java 描述语言

```
<script type="text/javascript">
     document.write("When  positive numbers are passed"+
                    " as parameters: " + Math.max(10, 32, 2));
</script>
```

*   **输出:**

```
When  positive numbers are passed as parameters: 32
```

**Math.max()** 方法用于返回零个或多个数字中的最大值。如果没有传递参数，则结果为“-Infinity”，如果至少有一个参数不能转换为数字，则结果为 NaN。
max()是一种静态的数学方法，因此，它总是被用作 Math.max()，而不是被创建的 Math 对象的方法。
**语法:**

```
Math.max(value1, value2, ...)
```

**参数:**该方法接受如上所述可使用 n 次的单一参数，描述如下:

*   **值:**该值发送给 **math.max()** 方法求最大值。

**返回值:**方法返回给定数字中最大的一个。
以下示例说明了 JavaScript 中的 Math max()方法:

*   **例 1:**

```
Input : Math.max(10, 32, 2)
Output: 32
```

*   **例 2:**

```
Input : Math.max(-10, -32, -1)
Output: -1
```

*   **例 3:**

```
Input : Math.max()
Output: -Infinity
```

*   **例 4:**

```
Input : Math.max(10,2,NaN)
Output: NaN
```

以上方法的更多代码如下:
**程序 1:** 当负数作为参数传递时。

## java 描述语言

```
<script type="text/javascript">
         document.write("Result : " + Math.max(-10, -32, -1));
</script>
```

**输出:**

```
Result : -1
```

**程序 2:** 无参数通过时。

## java 描述语言

```
<script type="text/javascript">
         document.write("Result : " + Math.max());
</script>
```

**输出:**

```
Result : -Infinity
```

**程序:**当 NaN 作为参数传递时。

## java 描述语言

```
<script type="text/javascript">
         document.write("Result : " + Math.max(10,2,NaN));
</script>
```

**输出:**

```
Result : NaN
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队