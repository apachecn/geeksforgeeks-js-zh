# JavaScript intl . collator . prototype . compare()方法

> 原文:[https://www . geesforgeks . org/JavaScript-intl-collator-prototype-compare-method/](https://www.geeksforgeeks.org/javascript-intl-collator-prototype-compare-method/)

这个 int l . collator . prototype . compare()方法基本上是用来按照 collator 对象的排序顺序对两个字符串进行比较的。

这里 **compare-getter** 函数根据排序器对象的排序顺序给出一个数字作为两个字符串之间的第一个字符串和第二个字符串进行比较，如果第一个字符串在第二个字符串之前，则显示一个小于 0 的值，如果第一个字符串在第二个字符串之后，则显示一个大于 0 的值，如果两个参数字符串相等，则显示 0。

**语法:**

```
collator.compare(firststring, secondstring)
```

**参数:**该方法将两个字符串**(第一个字符串，第二个字符串)**作为输入参数进行比较。

**示例 1:** 使用 **compare-getter** 函数对数组进行排序，该函数被限定在排序器之后，排序器进一步直接传递给 **Array.prototype.sort()** 。

## java 描述语言

```
<script>
  var x = ['Geeks', 'Geeksfor', 'GFG', 'courses', 'java'];
  var collator = new Intl.Collator('de-u-co-phonebk');

  // Using collator compare function
  x.sort(collator.compare);
  console.log(x.join(', '));
</script>
```

**输出:**

```
courses, Geeks, Geeksfor, GFG, java
```

**示例 2:** 同样使用 **compare-getter** 函数来搜索给定参数字符串之间的匹配字符串。让我们看看如何:

## java 描述语言

```
<script>
  var x = ['GFG-for-GFG', 'stress', 'Care', 'surprise', 'gfg'];
  var collator = new Intl.Collator('fr',
                     { usage: 'search', sensitivity: 'base' });

  var srch = 'gfg';
  var mtchs = x.filter(n => collator.compare(n, srch) === 0);
  console.log(mtchs.join(', '));
</script>
```

**输出:**

```
gfg
```