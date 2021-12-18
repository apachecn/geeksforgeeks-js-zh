# 在 JavaScript 中析构对象时如何设置默认值？

> 原文:[https://www . geeksforgeeks . org/如何在 javascript 中设置对象析构时的默认值/](https://www.geeksforgeeks.org/how-to-set-default-values-when-destructuring-an-object-in-javascript/)

**JavaScript 中的析构:**ECMA 脚本 6 版本引入了析构。这是一个用于将数组和对象中的值解包或释放到变量中的概念。对应于数组元素或对象属性的值存储在变量中。

**示例:**

## java 描述语言

```
var a, b;
[a, b] = [10, 20];

console.log(a);

console.log(b);
```

**输出:**

```
10
20
```

**在数组中:**在数组中，相应元素的值存储在变量中。

**示例 1:** 为了在数组中应用析构概念时给出数组中的默认值，我们需要用某个值初始化值。这样，默认值将被分配给变量。下面是通过这个概念的一个例子实现的。

## java 描述语言

```
let a, b, c ;
[a, b,c = 30] = [10, 20];

console.log(a);

console.log(b);

console.log(c);
```

**输出:**

```
10
20
30
```

**示例 2:** 如果相应变量存在任何值，则取该值，否则取默认变量。下面的代码片段以更清晰和详细的方式解释了这些行为。

## java 描述语言

```
let a, b, c;
[a, b,c = 30] = [10, 20, 50];

console.log(a);

console.log(b);

console.log(c);
```

**输出:**如果该数组中没有‘50’，那么‘c’的值将为‘30’。

```
10
20
50
```

**在对象中:**相应属性的值存储在变量中。

**例 1:** 对象中析构的应用和实现也和数组中的一样。下面是关于如何在对象中使用默认值的两个代码片段。

## java 描述语言

```
const student = {
    name: "Krishna"
}
const { name, age = 18 } = student; 

console.log(name);

console.log(age);
```

**输出:**

```
Krishna
18
```

**例 2:**

## java 描述语言

```
const student = {
    name: "Krishna",
    age : 21
}
const { name, age = 18 } = student; 

console.log(name);

console.log(age);
```

**输出:**

```
Krishna
21 
```