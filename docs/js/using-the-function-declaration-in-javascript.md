# 使用 JavaScript 中的函数*声明

> 原文:[https://www . geesforgeks . org/using-function-declaration-in-JavaScript/](https://www.geeksforgeeks.org/using-the-function-declaration-in-javascript/)

**函数*声明**用于定义返回生成器对象的生成器。生成器对于异步编程非常强大，因为它们旨在解决回调问题。

在生成器中，使用 **yield** 关键字代替 return。yield 语句暂停函数的执行，并将一个值发送回调用方，但保留足够的状态，使函数能够从上次执行的状态恢复。因此，该函数在最后一次产量运行后立即继续执行。 **next()** 方法用来返回一个有两个属性的对象，done 和 value，可以用来进入生成器的下一个状态。

**语法:**

```
function* function_name(param1, param2...)
{
  function body
}
```

下面的例子演示了函数*声明的用法。

**例 1:**

## 超文本标记语言

```
<html>
<body>
  <script>

    // Declaring a generator function
    function* generator(i) {
      yield i;
      yield i + 50;
      yield i + 100;
    }

    // Initialize the generator
    const generate = generator(50);

    // Console out the object returned
    // by the next() method
    let nextValObj = generate.next();

    // Console out the value of the object
    console.log(nextValObj.value);

    // Console out next iterations
    // of the generator
    console.log(generate.next().value);
    console.log(generate.next().value);

    // This value would be undefined as
    // the last defined one is i + 100
    console.log(generate.next().value);
  </script>
</body>
</html>
```

**输出:**

```
50
100
150
undefined
```

**例 2:**

## 超文本标记语言

```
<html>
<body>
  <script>
    function* powerup(n) {
      for (let num = n; ; num *= n) {

        // Yield out the current number
        yield num;
      }
    }
    for (let power of powerup(5)) {

      // Break if the number is
      // more than 1024
      if (power > 1024)
        break;

      console.log("Yielded:", power)
    }
  </script>
</body>
</html>
```

**输出:**

```
Yielded: 5
Yielded: 25
Yielded: 125
Yielded: 625
```