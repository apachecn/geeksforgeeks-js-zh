# JavaScript |函数*表达式

> 原文:[https://www . geesforgeks . org/JavaScript-function-expression-2/](https://www.geeksforgeeks.org/javascript-function-expression-2/)

**函数*** 是 JavaScript 中内置的关键字，用于定义表达式中的生成器函数。

**语法:**

```
function* [name]([param1[, param2[, ..., paramN]]]) {
   statements
}
```

**参数:**该功能接受如下参数，如上所述，如下所述:

*   **名称:** 此参数为 功能名。
*   **参数:** 该参数是要传递给函数的参数的 名称。
*   **语句:** 这些参数是组成身体的功能。

以下示例说明了 JavaScript: 中的 **函数*** 表达式

**例 1:**

## java 描述语言

```
<script>
    // Illustration of function* expression
    // use of function* keyword
    function* func() {
      yield 1;
      yield 2;
      yield 3;
      yield " - Geeks";
    }

    let obj = '';

    // Function calling
    for (const i of func()) {
          obj = obj + i;
    }

    // Output
    console.log(obj);
</script>
```

**输出:**

```
123 - Geeks
```

**例 2:**

## java 描述语言

```
<script>
    // Illustration of function* expression
    // use of function* keyword
    function* func2(y){
       yield  y * y;
    };

    function* func1(){
      for (let i = 1; i < 6; i++)
      {
        yield* func2(i);
      }
    };

    // Function calling
    for (const x of func1()) {

      // Output
      console.log(x);
    }
</script>
```

**输出:**

```
 1
 4
 9
 16
 25
```

**支持的浏览器:**JavaScript**函数*表达式**支持的浏览器如下:

*   谷歌 Chrome 49 及以上
*   边缘 12 及以上
*   Firefox 26 及以上版本
*   歌剧 36 及以上
*   Safari 10 及以上