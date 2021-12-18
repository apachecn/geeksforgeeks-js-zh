# JavaScript 数学 PI 属性

> 原文:[https://www.geeksforgeeks.org/javascript-math-pi-property/](https://www.geeksforgeeks.org/javascript-math-pi-property/)

下面是**数学 PI** 属性的例子。

*   **Example:**

## Javascript

```
<script>
  // Here value of Math.PI is printed.
  document.write(Math.PI);
</script>
```

**输出:**

```
3.141592653589793
```

数学。圆周率是 JavaScript 中的一个属性，简单来说就是用来求圆周率的值，也就是符号形式的π，它不过是圆的周长与直径的比值，其值大约为 3.141。它主要用于一道数学题。

**语法:**

```
Math.PI
```

**返回值:**它只是返回 PI 的值，即π

下面的例子说明了 JavaScript 中的数学 PI 属性。

**示例:**这里简单地将π的值显示为输出。

```
Input : Math.PI
Output : 3.141592653589793
```

上述属性的更多代码如下:

**程序 1:**PI 即π的值可以如下所示的函数形式打印出来。

## Javascript

```
<script>
  // function is being called.
  function get_Value_of_PI()
  {
      return Math.PI;
  }

  // function is calling.
  document.write(get_Value_of_PI());
</script>
```

**输出:**

```
3.141592653589793
```

**程序 2:** 这里我们考虑数学。PI 作为一个函数，但实际上它是一个属性，这就是为什么误差作为输出被显示。

## Javascript

```
<script>
  // Here we consider Math.PI as a function but
  // in actual it is a property that is why error
  // as output is being shown.
  document.write(Math.PI(12));
</script>
```

**输出:**

```
Error: Math.PI is not a function
```

**程序 3:** 每当我们需要找到与圆周率相关的任何东西的值时，我们都会借助这个属性。在数学上，它需要很多。这里我们要用给定的半径值来求圆的面积值。

## Javascript

```
<script>
  // function is being called with radius 5 as a parameter.
  function area_of_circle(radius_of_the_circle)
  {
      return Math.PI * radius_of_the_circle * radius_of_the_circle;
  }

  // Here area of the circle is 5 unit.
  document.write(area_of_circle(5));
</script>
```

**输出:**

```
78.53981633974483
```

**支持的浏览器:**

*   谷歌铬
*   Internet browser
*   red fox
*   歌剧
*   旅行队