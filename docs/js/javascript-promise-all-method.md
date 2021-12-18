# JavaScript | Promise.all()方法

> 原文:[https://www . geesforgeks . org/JavaScript-promise-all-method/](https://www.geeksforgeeks.org/javascript-promise-all-method/)

**Promise.all()方法**实际上是一个将一系列承诺(一个可迭代的)作为输入的承诺。它返回一个单一的**承诺**，当所有承诺都作为可重复传递时，或者当可重复传递不包含任何承诺时，该承诺将被解析。简单地说，如果任何传递的承诺被拒绝， **Promise.all()** 方法异步拒绝已经被拒绝的承诺的值，不管其他承诺是否已经解决。
**语法:**

```
Promise.all( iterable )
```

**参数:**该方法接受单个参数**可迭代**，该参数采用*承诺的数组*或包含一些对象的普通数组。
**返回值:**返回单个承诺遵循一些规则:

*   如果传递的参数为空，则返回一个已经*解析*的承诺。
*   如果传递的 iterable 不包含任何承诺，它将返回异步解析*的承诺。*
*   *对于所有其他情况，它返回一个待定的承诺。*

***履行与拒绝承诺. all()方法:**
**履行:**返还的承诺履行完毕，* 

*   *如果传递的 iterable 为空，则此方法同步返回一个已经解析的承诺。*
*   *如果所有通过的承诺都实现了，那么返回的承诺就会异步实现。*

***拒绝:**如果任何通过的承诺被拒绝，则无论其他承诺是否已经解决，该方法都拒绝该承诺的价值。
以下示例说明了 JavaScript Promise.all()方法:
**示例 1:** Promise.all 等待**履行**T8】*

## *java 描述语言*

```
*<script>
    p1 = Promise.resolve(50);
    p2 = 200
    p3 = new Promise(function(resolve, reject) {
        setTimeout(resolve, 100, 'geek');
    });

    Promise.all([p1, p2, p3]).then(function(values) {
        document.write(values);
    });
</script>*
```

***输出:*** 

```
*50, 200, geek*
```

***示例 2:** 这里 Promise.all 在 2000 ms 后解析，输出显示为数组。* 

## *java 描述语言*

```
*<script>
// Simple promise that resolves
// after a given time
const tOut = (t) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(`Completed in ${t}`)
    }, t)
  })
}

// Resolving a normal promise
tOut(1000).then(result => document.write(result+"<br>"))
// Completed in 1000

// Promise.all
Promise.all([tOut(1000), tOut(2000)]).then(result => document.write(result))
</script>*
```

***输出:*** 

```
*Completed in 1000
Completed in 1000, Completed in 2000*
```

*在这里， **Promise.all** 是维持承诺的顺序。数组中的第一个承诺将解析为输出数组的第一个元素，第二个承诺将是输出数组中的第二个元素，依此类推。
**例 3:** 这里**承诺，所有**等待，直到所有承诺解决。* 

## *java 描述语言*

```
*<script>
// Simple promise that resolves after a given time
const tOut = (t) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      resolve(`Completed in ${t}`)
    }, t)
  })
}

// Array contains some time duration
const durations = [1000, 2000, 3000]

const promises = []  // Empty array

durations.map((duration) => {

    // Calling the async function timeout(), so
    // at this point the async function has started
    // and enters the 'pending' state
    // pushing the pending promise to an array.
  promises.push(tOut(duration))
})

document.write(promises)

// Passing an array of pending promises to Promise.all
// Promise.all will wait till all the promises get resolves
// and then the same gets resolved.
Promise.all(promises).then(response => document.write(response))

// It prints after previous promises gets resolved
// ["Completed in 1000", "Completed in 2000", "Completed in 3000"]
</script>*
```

***输出:*** 

```
*[object Promise], [object Promise], [object Promise]
.
.
. (gap between previous and last promises)
.
.
Completed in 1000, Completed in 2000, Completed in 3000*
```

***例 4:** 如果其中一个承诺失败，那么其余所有承诺都会失败。然后**承诺.一切**被拒绝。* 

## *java 描述语言*

```
*<script>
// Promise that resolves after a given time
const tOut = (t) => {
  return new Promise((resolve, reject) => {
    setTimeout(() => {
      if (t === 2000) {
        reject(`Rejected in ${t}`)
      } else {
        resolve(`Completed in ${t}`)
      }
    }, t)
  })
}

const durations = [1000, 2000, 3000]

// Array contains some time durations
const promises = [] //empty array

durations.map((duration) => {
    promises.push(tOut(duration))
    // Pushing durations in the promises array
})

// Passing an array of pending promises to Promise.all
Promise.all(promises).then(response => document.write(response))
// Promise.all cannot be resolved, as one of the
// promises passed, got rejected.

.catch(error => document.write(`::Error::<br> ${error}`))
// Promise.all throws an error.
</script>*
```

***输出:*** 

```
*Error
Rejected in 2000*
```

***支持的浏览器:**JavaScript promise . all()方法支持的浏览器如下:*

*   *谷歌 Chrome 6.0 及以上版本*
*   *Internet Explorer 9.0 及以上版本*
*   *Mozilla 4.0 及以上版本*
*   *Opera 11.1 及以上*
*   *Safari 5.0 及以上版本*