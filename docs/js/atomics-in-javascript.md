# JavaScript 中的原子

> 原文:[https://www.geeksforgeeks.org/atomics-in-javascript/](https://www.geeksforgeeks.org/atomics-in-javascript/)

**Atomics:** Atomics 是一个 JavaScript 对象，它赋予原子任务以静态策略进行。与数学对象的策略一样，原子的技术和属性也是静态的。原子与 SharedArrayBuffer 对象一起使用。原子活动是在原子模块中引入的。与世界范围内的其他文章相比，Atomics 不是一个构造器。原子不能被另一个管理员使用，也不能作为一种能力被召唤。

**原子操作:**原子操作不是连续的。共享内存时，多线程可以在内存中读写数据。如果任何数据发生变化，就会出现数据丢失。原子操作确保数据按照预测值写入和准确读取。在当前操作完成和原子操作开始之前，无法更改现有信息。

**方法:**

*   [**atomics . add():**](https://www.geeksforgeeks.org/atomics-add-javascript/)**将提供的值添加到指定数组索引中的当前值。返回旧的索引值。**
*   **[**【atomics . AND():**](https://www.geeksforgeeks.org/atomics-and-in-javascript/)**【AND】值是根据提供的值指定的数组索引按位计算的。返回该索引的旧值。****
*   ****[**atomics . exchange():**](https://www.geeksforgeeks.org/atomics-exchange-javascript/)**在指定的数组索引处指定一个值。返回旧值。******
*   ******[**atomics . compare exchange():**](https://www.geeksforgeeks.org/atomics-compareexchange-javascript/)**如果值相同，则指定指定数组索引中的值。旧值返回。********
*   ******[**Atomics.isLockFree(大小):**](https://www.geeksforgeeks.org/atomics-islockfree-javascript/) 原始优化，确定是使用锁还是原子操作。如果在给定元素大小的数组中执行硬件原子操作(与锁相反)，则返回 true。******
*   ****[**atomics . load():**](https://www.geeksforgeeks.org/atomics-load-javascript/)**该值返回指定的数组索引。******
*   ********Atomics.or():** 按位 or 计算指定数组索引处给定值的值。返回旧的索引值。******
*   ****[**atomics . Notify():**](https://www.geeksforgeeks.org/javascript-atomics-notify-method/)**通知等待指定数组索引的代理。返回通知的座席数。******
*   ******[**atomics . sub():**](https://www.geeksforgeeks.org/atomics-sub-javascript/)**删除指定数组索引处的值。返回旧的索引值。********
*   ******[**atomics . store():**](https://www.geeksforgeeks.org/atomics-store-javascript/)**在指定的数组索引上保存一个值。返回值。********
*   ******[**atomics . wait():**](https://www.geeksforgeeks.org/javascript-atomics-wait-method/)**验证指定的数组索引仍然有值，并且等待或等待时间正在休眠。返回“确定”、“不一样”或“超时”如果调用代理无法等待，它会抛出一个错误异常。********
*   ******[**atomics . XOR():**](https://www.geeksforgeeks.org/atomics-xor-javascript/)**计算给定数组索引上给定值的按位异或。返回旧的索引值。********

********例 1:********

## ****java 描述语言****

```
**var buffer = new 
// create a SharedArrayBuffer
SharedArrayBuffer(50); 
var a = new Uint8Array(buffer);
// Initialising element at zeroth position of array with 9 
a[0] = 9;
console.log(Atomics.load(a, 0)); 
// Displaying the return value of the Atomics.store() method
console.log(Atomics.store(a, 0, 3)); 
// Displaying the updated SharedArrayBuffer 
console.log(Atomics.load(a, 0));**
```

******输出:******

```
**933**
```

******例 2:******

## ****java 描述语言****

```
**const buffer = new SharedArrayBuffer(2048);

const ta = new Uint8Array(buffer);

ta[0]; // 0

ta[0] = 5; // 5

Atomics.add(ta, 0, 12);   // 5

Atomics.load(ta, 0);      // 17

Atomics.and(ta, 0, 1); // 17

Atomics.load(ta, 0); // 1

Atomics.exchange(ta, 0, 12); // 1

Atomics.load(ta, 0); // 12

Atomics.compareExchange(ta, 0, 5, 12); // 1

Atomics.load(ta, 0); // 1

Atomics.isLockFree(1); // true

Atomics.isLockFree(2); // true

Atomics.or(ta, 0, 1); // 12

Atomics.load(ta, 0);  // 13

Atomics.store(ta, 0, 12); // 12

Atomics.sub(ta, 0, 2); // 12

Atomics.load(ta, 0); // 10

Atomics.xor(ta, 0, 1); // 10

Atomics.load(ta, 0); // 11**
```

******输出:******

```
**5
17
17
1
1
12
1
1
True
True
13
13
12
12
10
10** 
```