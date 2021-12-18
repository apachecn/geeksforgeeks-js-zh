# JavaScript 数学 tan()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-tan-method/](https://www.geeksforgeeks.org/javascript-math-tan-method/)

下面是**数学 tan()** 方法的例子。

*   **示例:**

## java 描述语言

```
<script type="text/javascript">
    document.write("When  zero is  passed as a parameter: "
      + Math.tan(0));
</script>
```

**输出:**

```
When  zero is  passed as a parameter: 0

```

Javascript 中的 **Math.tan()** 方法用来返回一个数的正切值。
math . tan()方法返回一个代表角度正切值的数值。tan()是 Math 的静态方法，因此，它总是用作 Math.tan()，而不是作为创建的 Math 对象的方法。

**语法:**

```
Math.tan(value)

```

**参数:**该方法接受如上所述的单个参数，如下所述:

*   **值**是一个以弧度表示角度的数字。

**返回:**方法返回给定数字的正切值。

下面的例子说明了 JavaScript 中的数学 tan()方法:

*   **例 1:**

```
Input : Math.tan(0)
Output : 0

```

*   **例 2:**

```
Input : Math.tan(1)
Output : 1.557407724654902

```

*   **例 3:**

```
Input : Math.tan(Math.PI / 4)
Output : 0.9999999999999999

```

上述方法的更多代码如下:

**程序 1:** 当 1 作为参数传递时。

## java 描述语言

```
<script type="text/javascript">
    document.write("Result : " + Math.tan(1));
</script>
```

**输出:**

```
Result : 1.557407724654902

```

**程序 2:** 当 PI 作为参数传递时。

## java 描述语言

```
<script type="text/javascript">
    document.write("Result : " + Math.tan(Math.PI / 4));
</script>
```

**输出:**

```
Result : 0.9999999999999999

```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队