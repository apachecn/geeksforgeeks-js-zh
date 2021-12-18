# JavaScript 数组过滤器()方法

> 原文:[https://www . geesforgeks . org/JavaScript-数组-过滤器-方法/](https://www.geeksforgeeks.org/javascript-array-filter-method/)

下面是**数组过滤器()**方法的例子。

*   **例:**

## Java Script 语言

```
<script>
    // JavaScript to illustrate findIndex() method
    function canVote(age) {
        return age >= 18;
    }

    function func() {
        var filtered = [24, 33, 16, 40].filter(canVote);
        document.write(filtered);
    }
    func();
</script>                    
```

*   **输出:**

```
[24,33,40]

```

**arr.filter()** 方法用于根据给定的数组创建新的数组，该数组只包含给定数组中满足参数方法设置的条件的元素。
**语法:**

```
array.filter(callback(element, index, arr), thisValue)

```

**参数:**该方法接受上述五个参数，描述如下:

*   **回调:**该参数保存数组每个元素要调用的函数。
*   **元素:**参数保存当前正在处理的元素的值。
*   **索引:**这个参数是可选的，它保存数组中从 0 开始的 currentValue 元素的索引。
*   **arr:** 此参数是可选的，它保存调用 array . after 的完整数组。
*   **此值:**此参数是可选的，它保存要传递的上下文，以便在执行回调函数时使用。如果传递了上下文，它将像这样用于回调函数的每次调用，否则使用 undefined 作为默认值。

**返回值:**该方法返回一个新数组，该数组只包含那些满足 **arg_function** 条件的元素。
以下示例说明了 JavaScript 中的 **arr.filter()** 方法:

*   **示例 1:** 在此示例中，方法**过滤器()**创建一个新数组，该数组仅由满足 **isPositive()** 函数检查的条件的元素组成。

```
function isPositive(value) {
  return value > 0;
}

var filtered = [112, 52, 0, -1, 944].filter(isPositive);
print(filtered);

```

*   **输出:**

```
[112,52,944]

```

*   **示例 2:** 在此示例中，方法**过滤器()**创建一个新数组，该数组仅由满足 **isPositive()** 函数检查的条件的元素组成。

```
function isEven(value) {
  return value % 2 == 0;
}

var filtered = [11, 98, 31, 23, 944].filter(isEven);
print(filtered);

```

*   **输出:**

```
[98,944]

```

上述方法的代码定义如下:
**程序 1:**

## Java Script 语言

```
<script>
    // JavaScript to illustrate filter() method
    function isPositive(value) {
        return value > 0;
    }

    function func() {
        var filtered = [112, 52, 0, -1, 944].filter(isPositive);
        document.write(filtered);
    }
    func();
</script>
```

**输出:**

```
[112,52,944]

```

**节目 2:**

## Java Script 语言

```
<script>
    // JavaScript to illustrate filter() method
    function isEven(value) {
        return value % 2 == 0;
    }

    function func() {
        var filtered = [11, 98, 31, 23, 944].filter(isEven);
        document.write(filtered);
    }
    func();
</script>
```

**输出:**

```
[98,944]

```

**支持的浏览器:**JavaScript**数组过滤器()**方法支持的浏览器如下:

*   谷歌 Chrome
*   微软边缘 9.0
*   Mozilla Firefox 1.5
*   旅行队
*   歌剧