# JavaScript 数学 acos()方法

> 原文:[https://www.geeksforgeeks.org/javascript-math-acos-method/](https://www.geeksforgeeks.org/javascript-math-acos-method/)

下面是**数学 acos( )** 方法的例子。

*   **例:**

## java 描述语言

```
<script type="text/javascript">
         document.write("When 1 is  passed as a parameter: "
                        + Math.acos(1));
</script>
```

*   **输出:**

```
When 1 is  passed as a parameter: 0
```

**Math.acos( )** 方法用于返回以弧度为单位的数字的反余弦。Math.acos()方法返回一个介于 0 和π弧度之间的数值。数学 acos()是数学的静态方法，因此，它总是被用作数学 acos()，而不是创建数学对象的方法。

> math . acos(x)= arccos(x)=唯一 y，
> 其中 y 属于[0；π]
> 使得 cos(y)=x

**语法:**

```
Math.acos(value)
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **值**是一个弧度数，你想找谁反余弦。

**返回:****math . acos()**函数返回给定弧度数的反余弦值。
以下示例说明了 JavaScript 中的 Math acos()方法:

*   **例 1:**

```
Input  : Math.acos(1)
Output : 0
```

*   **例 2:**

```
Input  : Math.acos(-1)
Output : 3.141592653589793
```

*   **例 3:**

```
Input : Math.acos(0)
Output: 1.5707963267948966
```

以上方法的更多示例代码如下:
**程序 1:**

## java 描述语言

```
<script type="text/javascript">
         document.write("When -1 is  passed as a parameter: "
                        + Math.acos(-1));
</script>
```

**输出:**

```
When 1 is  passed as a parameter: 3.141592653589793
```

**节目 2:**

## java 描述语言

```
<script type="text/javascript">
         document.write("When 0 is  passed as a parameter: "
                        + Math.acos(0));
</script>
```

**输出:**

```
When 0 is  passed as a parameter: 1.5707963267948966
```

**节目 3:**

## java 描述语言

```
<script type="text/javascript">
         document.write("When 0.5 is  passed as a parameter: "
                        + Math.acos(0.5));
</script>
```

**输出:**

```
When 0.5 is  passed as a parameter: 1.0471975511965979
```

**节目 4:**

## java 描述语言

```
<script type="text/javascript">
         document.write("When 2 is  passed as a parameter: "
                        + Math.acos(2));
</script>
```

**输出:**

```
When 2 is  passed as a parameter: NaN
```

**支持的浏览器:**

*   谷歌 Chrome
*   微软公司出品的 web 浏览器
*   火狐浏览器
*   歌剧
*   旅行队