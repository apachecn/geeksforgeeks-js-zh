# 洛达什 _。节气门()方法

> 原文:[https://www.geeksforgeeks.org/lodash-_-throttle-method/](https://www.geeksforgeeks.org/lodash-_-throttle-method/)

**Lodash** 是一个工作在下划线. js 之上的 JavaScript 库，Lodash 有助于处理数组、字符串、对象、数字等。

**_。lodash 中的 throttle()** **方法**用于创建一个 throttled 函数，该函数每等待毫秒最多只能调用 func 参数一次。这里的节流函数有一个 cancel 方法，用于取消被延迟的 func 调用，它还有一个 flush 方法，用于立即调用被延迟的 func。此外，它还提供了一些选项，用于暗示是否应该在等待超时的前沿和/或后沿调用所述函数。

**语法:**

```
_.throttle(func, wait, options)
```

**参数:**该方法接受三个参数，如上所述，如下所述:

*   **功能:**是需要节流的功能。
*   **等待:**是要抑制呼叫的毫秒数。
*   **选项:**是选项对象。
    *   **options.leading:** 它定义了在超时前沿的调用。
    *   **选项.尾随:**它定义了在超时的后沿调用。

**返回值:**该方法返回新的节流函数。

**注意:**

*   Here, func is called with the last parameter of the throttle function. However, a subsequent call to the throttle function will return the result of the last function call.
*   Here, if the leading and trailing options are true, then func will be called at the trailing edge of the timeout if and only if the throttle function is called several times during the whole waiting timeout period.
*   Here, if the waiting time is 0 and the leading option is false, the func call is delayed to the next scale.

**例 1:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling throttle() method with its parameter
var throt_fun = _.throttle(function () {
        console.log('Function throttled after 1000ms!');
    }, 1000);

throt_fun();
```

**输出:**这里，1000 毫秒后功能被节流后，因为这里的等待时间是 1000 毫秒。

```
Function throttled after 1000ms!
```

**例二:**

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling throttle() method with its parameter
var throt_fun = _.throttle(function() {
        console.log('Function throttled after 1000ms!');
    }, 1000);

// Defining loop
var loop = function() {
    setTimeout(loop, 5)
    throt_fun();
};

// Calling loop to start
loop();
```

**输出:**所以，在这里，循环直到你手动停止才停止。

```
Function throttled after 1000ms!
Function throttled after 1000ms!
Function throttled after 1000ms!
Function throttled after 1000ms!
Function throttled after 1000ms!
Function throttled after 1000ms!
.
.
.
.
// So on until you stop it manually.

```

**示例 3:** 这里，在超时的后沿调用函数。

## Javascript

```
// Requiring lodash library
const _ = require('lodash');

// Calling throttle() method with its parameter
var throt_fun = _.throttle(function () {
    console.log('Function is called on the'
        + ' trailing edge of the timeout '
        + 'and throttled after 2000ms!');
    }, 2000, { 'trailing': true });

throt_fun();
```

**输出:**

```
Function is called on the trailing edge of the 
timeout and throttled after 2000ms!
```

**参考:**T2】https://lodash.com/docs/4.17.15#throttle