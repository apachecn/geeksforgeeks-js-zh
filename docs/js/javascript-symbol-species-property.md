# JavaScript 符号.物种属性

> 原文:[https://www . geesforgeks . org/JavaScript-symbol-species-property/](https://www.geeksforgeeks.org/javascript-symbol-species-property/)

Symbol.species 属性指定构造函数用来创建派生对象的函数值属性。这样，我们就可以创建一个派生对象。

**语法:**

```
[Symbol.species]
```

**属性:**物种访问器属性可用于允许子类覆盖对象的默认构造函数。

下面的例子说明了 JavaScript 中的 Symbol.species 属性。

**例 1:**

## java 描述语言

```
<script>

  // Created geek class that is extended by Array
  class geek extends Array {
    static get [Symbol.species]() {
      return Array;
    }
  }

  // Values assigned to geek
  const a = new geek(1, 2, 3, 4);
  //mapped values to geek object
  const mapped = a.map((x) => 2);

  console.log(mapped instanceof geek);
  //  output: false

  console.log(mapped instanceof geek);
  // output: false
</script>
```

**输出:**

```
false
false
```

**例 2:**

## java 描述语言

```
<script>
  class geek extends Array {

    // Overwrite species to the parent Array constructor
    static get [Symbol.species]() {
      return Array;
    }
  }
  let a = new geek(1, 2, 3, 5, 7, 8);
  let mapped = a.map((x) => x);

  console.log(mapped instanceof geek); // false
  console.log(mapped instanceof Array); // true
</script>
```

**输出:**

```
false
true
```