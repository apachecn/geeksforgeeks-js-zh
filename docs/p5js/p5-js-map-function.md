# p5.js 地图()功能

> 原文:[https://www.geeksforgeeks.org/p5-js-map-function/](https://www.geeksforgeeks.org/p5-js-map-function/)

p5.js 中的 map()函数用于在 min2 到 max2 的范围内对 min1 到 max1 的数字进行归一化。

如果您正在缩放元素，规范化在 p5.js 中非常有用。因为正如我们所知，归一化处理了缩放中的所有比例，所以我们得到了一个完全平衡的缩放。

不仅仅是缩放，而且在任何转换操作中，规范化都非常有帮助。

**语法:**

```
map(value, start1, stop1, start2, stop2, [withinBounds])
```

**参数:**该功能接受六个参数，如上所述，描述如下:

*   **值:**要归一化的值。
*   **min1:** 该值当前范围的最小值。
*   **max1:** 值的当前范围的最大值。
*   **min2:** 数值目标范围的最小值。
*   **max2:** 数值目标范围的最大值。
*   **在边界内(可选):**这将值的归一化值限制在[min2，max2]的范围内。

**示例 1:** 默认情况下，WithinBounds 为 false。

## java 描述语言

```
function setup() {
    noLoop();
}

function draw() {

    background(220);

    // Assume value has range [0, 100]
    let value = 50;

    // We want to convert value 
    // in range of [0, 50]
    let newValue = map(value, 0, 100, 0, 50);

    console.log(newValue);
}
```

**输出:**

```
25
```

**示例 2:** 注意在边界约束范围内的值

## java 描述语言

```
function setup() {
    noLoop();
}

function draw() {

    background(204);

    // Value has a range[0, 100]
    let value = 150;

    // We are mapping it in range of [0, 50]
    let newValue1 = map(value, 0, 100, 0, 50);

    console.log(newValue1);

    // Notice the last parameter is true
    // we are mapping it in range of [0, 50]
    let newValue2 = map(value, 0, 100, 0, 50, true);

    console.log(newValue2);
}
```

**输出:**

```
75
50
```