# 如何获取 JavaScript 中第一个非空/未定义的参数？

> 原文:[https://www . geeksforgeeks . org/如何获取第一个非空-未定义-javascript 中的参数/](https://www.geeksforgeeks.org/how-to-get-the-first-non-null-undefined-argument-in-javascript/)

在很多情况下，我们可以找到传递给函数的第一个非空或非未定义的参数。这就是所谓的聚结。

**方法 1:** 我们可以在 ES6 之前的 JavaScript 中通过循环遍历参数并检查哪个参数等于 NULL 来实现合并。然后，我们立即返回非空的参数。

**示例:**

## java 描述语言

```
<script>
function coalesce() {
  for (let i = 0; i < arguments.length; i++) {
    if (arguments[i] != null) {
      return arguments[i];
    }
  }
}

console.log(
  coalesce(null, undefined, "First",
           1, 2, 3, null)
);
</script>
```

**输出:**

```
First
```

**方法 2:** 我们可以用 ES6 替代上述方法，达到类似的效果。使用 ES6 中的 Rest 参数，我们收集了*参数*中的所有参数。我们传递一个胖箭头函数作为 find 方法的回调，该函数遍历*参数*的每个元素。我们使用 _ identifier 中的一次性变量作为 find 方法回调中的元素标识符。最后，我们使用 **includes()** 方法检查回调中由 _ 标识的元素是属于 *null* 还是属于 *undefined* 。第一个不符合测试的元素是我们的输出。

**示例:**

## java 描述语言

```
<script>
const coalesceES6 = (...args) =>
  args.find(_ => ![null,undefined].includes(_)
);

console.log(
  coalesceES6(null, undefined, "Value One",
              1, 2, 3, null)
);
</script>
```

**输出:**

```
Value One
```

**合并用例**

既然我们已经看到了如何实现聚结，让我们讨论一下它的一些用例。

**用例 1:** 填充对象数组中的空值/未定义值

**示例:**假设您有一个产品目录，其中包含大量产品列表。每个产品都有描述和总结。您希望通过从该数据库中提取数据来显示描述和摘要。在这种情况下，您可以使用带有两个参数的合并，当缺少摘要时，使用摘要值和截断的描述值来填充。

## java 描述语言

```
<script>
let products = [
  {
    id: 1,
    desc: `The best in class toaster that has 140
    watt power consumption with nice features that
    roast your bread just fine. Also comes bundled 
    in a nice cute case.`,
    summ: `Get world class breakfasts`,
  },
  {
    id: 2,
    desc: `A massager that relieves all your pains 
    without the hassles of charging it daily 
    or even hourly as it comes packed with Li-Ion
    batteries that last upto 8 hrs.`,
    summ: "Warm comfort for your back",
  },
  {
    id: 3,
    desc: `An air conditioner with a difference that
    not only cools your room to the best temperatures 
    but also provides cleanliness and disinfection at
    best in class standards`,
    summ: null,
  },
];

const coalesceES6 = (...args) =>
  args.find((_) => ![null, undefined].includes(_));

function displayProdCat(products) {
  for (let product of products) {
    console.log(`ID = ${product.id}`);
    console.log(`Description = ${product.desc}`);
    let summProd =
      coalesceES6(product.summ,
                  product.desc.slice(0, 50) + "...");
    console.log(`Summary = ${summProd}`);
  }
}

displayProdCat(products);
</script>
```

**输出:**通过合并，如果存在汇总值，将显示汇总值。如果缺少摘要(空或未定义)，合并函数将选择第二个参数，并在摘要字段中显示截断的描述。

```
ID = 1
Description = The best in class toaster that has 140
    watt power consumption with nice features that
    roast your bread just fine. Also comes bundled
    in a nice cute case.
Summary = Get world class breakfasts
ID = 2
Description = A massager that relieves all your pains
    without the hassles of charging it daily
    or even hourly as it comes packed with Li-Ion
    batteries that last upto 8 hrs.
Summary = Warm comfort for your back
ID = 3
Description = An air conditioner with a difference that
    not only cools your room to the best temperatures
    but also provides cleanliness and disinfection at
    best in class standards
Summary = An air conditioner with a difference that
    not ...
```

**用例 2:** 在表达式中缺少数值的情况下填充数值来执行计算

**例如:**假设你有一个一年的月收入数组，其中有几个缺失的值。现在，您想要找到总年收入，您决定用基本默认值 1000 替代缺少数据的月份。我们对每月数据数组应用缩减方法。我们将每次迭代的总和存储在累加器中，并稍加修改。我们对当前项目进行合并，并将月收入(如果存在)或默认值(如果月收入为空或未定义)添加到累加器中。

## java 描述语言

```
<script>
const incomeFigures = {
  default: 1000,
  monthWise: [1200, , 600, 2100, , 329,
              1490, , 780, 980, , 1210],
};

const coalesceES6 = (...args) =>
  args.find((_) => ![null, undefined].includes(_));

function yearlyIncome(incomeFig) {
  return incomeFig.monthWise.reduce(
    (total, inc) => total +
      coalesceES6(inc, incomeFig.default)
  );
}

console.log(
  `Yearly income equals 
  ${yearlyIncome(incomeFigures)}`
);
</script>
```

**输出:**

```
Yearly income equals 8689
```