# 解释 ES6 中的常数

> 原文:[https://www.geeksforgeeks.org/explain-constants-in-es6/](https://www.geeksforgeeks.org/explain-constants-in-es6/)

JavaScript 是世界上最流行的轻量级、解释编译的编程语言。它也被称为网页的脚本语言。它以开发网页而闻名，许多非浏览器环境也使用它。JavaScript 可以用于客户端开发和服务器端开发。

**Const 关键字:**在编程时，我们会遇到一些情况，我们希望声明一个变量，该变量的值在整个程序中保持不变。一个这样的例子是 pi 的值总是保持不变。ES6 支持一个这样的声明，可以使用单词 **const** 来声明。

声明*常量*变量的语法是:

```
const CONST_NAME = value;
```

**常量的属性:**

*   用 const 这个词声明的变量是**不可变的**。
*   用 const 声明的变量是**块范围的**。
*   不能重新分配用常量声明的变量**。**
*   用 const 声明的变量必须在声明后立即赋值。
*   用 const 声明的变量在声明前不能使用。

下面的例子将展示使用 const 关键字的各种属性。

**例 1:** 在本例中，将抛出一个错误为“试图覆盖常量‘I’”。因此，这表明不能重写用 const 声明的变量。

## java 描述语言

```
<script>
    const myFunc = function () {
        const i = 5;

        try {

            // The below line will throw an error
            i = i + 2;
        }
        catch (error) {
            console.log(error)
        }
    }
</script>
```

**输出:**

```
TypeError: Assignment to constant variable.
```

**示例 2:** 下面的语句还将显示“语法错误”，因为 const 变量的值必须仅在声明时定义。

## java 描述语言

```
// Will throw syntax error as
// no value has been assigned        
const MY_VAR;
```

**输出:**

```
SyntaxError: Missing initializer in const declaration
```

**示例 3:** 下面的语句还抛出了一个错误“未捕获语法错误”，因为我们试图声明一个使用已经声明为常量的变量名的。

## java 描述语言

```
// Declaring multiple const values
// with the same variable
const pi = 3.15;
const pi = 2.6;
```

**输出:**

```
SyntaxError: Identifier 'pi' has already been declared
```

**用对象声明常量:**通过将对象声明为常量，我们可以操纵对象的内部属性。

**例 4:**

## java 描述语言

```
const pair = {x:30, y:60};

// Updating the x and y values
// of the object
pair.x = 10;
pair.y = 90;

console.log(pair);
```

**输出:**

```
{
  x: 10,
  y: 90
}
```

常量对象的属性值可以被操作，但是您不能重新分配*常量*对象，如下例所示。

**例 5:**

## java 描述语言

```
const pair = { x: 30, y: 20 }

// Will throw an error that
// pair has already been declared
const pair = { a: 35 }
```

**输出:**

```
SyntaxError: Identifier 'pair' has already been declared
```

**示例 6:** 还可以如下所示向 const 对象添加新属性。

## java 描述语言

```
const pair = { x: 30, y: 20 }

// Adding a new property
// to the pair
pair.z = 67;

console.log(pair);
```

输出应该是这样的:

```
{
  x: 30,
  y: 20,
  z: 67
}
```

**Const with Loops:** ES6 支持在 for-of 循环中使用 Const，其中为每次迭代创建新的绑定。

**例 7:**

## java 描述语言

```
const arr = ['hi', 'how', 'are', 'you'];

// Looping through all the elements
// of the array
for (const ele of arr) {
    console.log(ele);
}
```

**输出:**

```
hi
how
are
you
```