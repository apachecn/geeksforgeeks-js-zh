# 如何优化 JavaScript 中的 switch 语句？

> 原文:[https://www . geesforgeks . org/如何优化 javascript 中的开关语句/](https://www.geeksforgeeks.org/how-to-optimize-the-switch-statement-in-javascript/)

[switch 语句](https://www.geeksforgeeks.org/switch-statement-in-java/)是某些编程任务所必需的，并且 switch 语句的功能在所有编程语言中是相同的。基本上，switch 语句根据给开关的期望条件来切换情况。当使用多个连续的 **if/else 语句**时，可以使用 Switch 语句。但是在某个地方 **if/else** 语句有益使用，在某个地方 **switch 语句**。因此，我们在 JavaScript 中优化了编程任务中的 switch 语句。

由于 JavaScript 会多次遍历整个案例分支，因此建议使用 break 来防止意外的案例匹配，或者避免引擎解析额外的代码。根据情况使用 **break** 的方法有很多，比如对于季节检查，某个特定的季节有一个多月，对于这种情况 **break** 可以根据情况在其他地方使用。

现在举个例子来理解 switch 语句。在这里，我们尝试使用开关获取工作日。
这里有两种情况可供比较:

*   如果/否则语句。
*   切换语句。

以下示例实现了这两种方法:

**例 1:**

```
<script>
let dayIndex = new Date().getDay();
let day;

if (dayIndex === 0) {
  day = 'Sunday';
}
else if (dayIndex === 1) {
  day = 'Monday';
}
else if (dayIndex === 2) {
  day = 'Tuesday';
}
else if (dayIndex === 3) {
  day = 'Wednesday';
}
else if (dayIndex === 4) {
  day = 'Thursday';
}
else if (dayIndex === 5) {
  day = 'Friday';
}
else if (dayIndex === 6) {
  day = 'Saturday';
};

console.log(day); // "Friday"
</script>
```

**示例 2:** 使用 if/else 真的很啰嗦，而且包含了很多 switch 可以轻松处理的不必要的样板文件。

```
<script>
let dayIndex = new Date().getDay();
let day;

switch (dayIndex) {
  case 0:
    day = "Sunday";
    break;
  case 1:
    day = "Monday";
    break;
  case 2:
    day = "Tuesday";
    break;
  case 3:
    day = "Wednesday";
    break;
  case 4:
    day = "Thursday";
    break;
  case 5:
    day = "Friday";
    break;
  case 6:
    day = "Saturday";
    break;
};

console.log(day); // "Friday"
</script>
```

**注意:** JavaScript 没有一个本机方法来获取星期几