# JavaScript Intl 方法

> 原文:[https://www.geeksforgeeks.org/javascript-intl-methods/](https://www.geeksforgeeks.org/javascript-intl-methods/)

下面是 [Intl](https://www.geeksforgeeks.org/javascript-intl-complete-reference/) 方法的一个例子。

*   **示例:**

## java 描述语言

```
<script>
function func(){

  // Original Array
  var arr = ['z', 's', 'l', 'm', 'c', 'a', 'b'];

  // Sorting Array
  var arr_sort = arr.sort(new Intl.Collator('en').compare)
  console.log(arr_sort);
}
func();
</script>
```

**输出:**

```
['a', 'b', 'c', 'l', 'm', 's', 'z']
```

**Intl 方法:****Intl()**方法是在构造函数的帮助下，将字符串*、数字、*日期*、*和时间以本地格式进行格式化。

**语法:**

```
new Intl.constructors(locales, options);
```

**论据:**

*   **语言环境参数:**语言环境参数用于确定操作中使用的语言环境。地区可能是:
    *   未定义:使用默认区域设置。
    *   区域设置:区域设置是构造函数用来标识语言或标记的标识符。
    *   区域设置列表:它是一个区域设置的集合。
*   区域设置由连字符分隔。区域设置可以包括:
    *   语言子标签。
    *   区域子标签。
    *   下标子标签。
    *   专用扩展语法。
    *   一个或多个 BCP 47 延伸序列。
    *   一个或多个变体子标签。
*   **示例:**
    *   “hi”:这是印地语的语言子标签。
    *   “de-AT”:德语的语言标签和奥地利地区标签的 AT。
    *   “zh-Hans-CN”:Hans 是中国区域的区域标签。
    *   “en-emoden”:en-emoden 是早期现代英语的变体标记。
*   **Options 参数:**Options 的参数是一个对象，其属性随不同的构造函数和函数而变化。如果选项的参数是未定义的，则使用所有属性的默认值。

**示例 1:** 不同构造函数的示例如下。在这个例子中，**国际机场。Collator()** 创建 Intl。帮助在任何集合的语言敏感排序中进行排序的排序器对象。由于我们用英语对数组进行排序，所以它是按字母顺序排序的。

```
var l = new Intl.Collator('en').compare
console.log(['z', 'b', 'e', 'o', 'a'].sort(l)); 
```

## java 描述语言

```
<script>

  // Javascript to illustrate Intl.Collator constructor
  function func() {

    // Creating object for which help in sorting
    var l = new Intl.Collator("en");

    // Sorting array
    var array = ["z", "b", "e", "o", "a"];
    var arr = array.sort(l.compare);
    console.log(arr);
  }
  func();
</script>
```

**输出:**

```
['a', 'b', 'e', 'o', 'z']
```

**例 2:** 在本例中，**国际机场。DateTimeFormat()** 构造函数创建一个**国际号码。DateTimeFormat** 对象，有助于区分语言的日期时间格式。这里的子标签是“en-US”，所以日期变量是美国英语的格式。

```
const date = new Date(Date.UTC(2021, 06, 10, 10, 20, 30, 40));
console.log(new Intl.DateTimeFormat('en-US').format(date));
```

## java 描述语言

```
<script>

  // Javascript to illustrate Intl.DateTimeFormat constructor
  function func() {

    // Creating Time variable
    const date = new Date(Date.UTC(2021, 06, 10, 10, 20, 30, 40));

    // Creating object for which help in Formatting
    const ti = new Intl.DateTimeFormat("en-US");

    // Formatting date
    const time = ti.format(date);
    console.log(time);
  }
  func();
</script>
```

**输出:**

```
7/10/2021
```

**例 3:** 在本例中，**国际机场。DisplayNames()** 构造函数创建一个**国际号码。显示名称**对象，帮助构造器翻译任何语言、区域和脚本显示名称。这里 **Intl** 根据地区用英语翻译‘UN’。

```
const rNames = new Intl.DisplayNames(['en'], { type: 'region' });
console.log(rNames.of('UN'));
```

## java 描述语言

```
<script>

  // Javascript to illustrate Intl.DisplayNames constructor
  function func() {

    // Creating object for translation
    const rNames = new Intl.DisplayNames(["en"], { type: "region" });

    // Translating into region language
    const a = rNames.of("UN");
    console.log(a);
  }
  func();
</script>
```

**输出:**

```
United Nations
```

**例 4:** 在本例中，**国际机场。ListFormat()** 创建一个 intl。列表格式对象，帮助设置列表格式。这里的子标签是“en ”,所以它是英文的，样式很长，类型是连词，所以格式化的列表有一些连接词。

```
const Names = ['Jack', 'Rahul', 'Bob'];
const format = new Intl.ListFormat('en', { style: 'long', type: 'conjunction' });
console.log(format.format(Names));
```

## java 描述语言

```
<script>

// Javascript to illustrate Intl.ListFormat constructor
function func(){

  // Orignal list
  const Names = ['Jack', 'Rahul', 'Bob'];

  // Creating object for list formatting
  const format = new Intl.ListFormat('en',
    { style: 'long', type: 'conjunction' });

  // Formating list
  const list = format.format(Names);
  console.log(list);
}
func();
</script>
```

**输出:**

```
Jack, Rahul, and Bob
```

**例 5:** 在本例中，**国际机场。Locale()** 构造函数为区域、语言和脚本创建一个 Locale 标识符。这里的子标签是“en-US”，因此它创建了美国英语地区语言区域标识符。

```
let us = new Intl.Locale('en-US');
console.log(us.baseName)
```

## java 描述语言

```
<script>

  // Javascript to illustrate Intl.Locale
  // constructor
  function func() {

    // Creating locale Object identifier
    let us = new Intl.Locale("en-US");

    // Printing baseName of identifier
    console.log(us.baseName);
  }
  func();
</script>
```

**输出:**

```
en-US 
```

**例 6:** 在本例中，**国际机场。NumberFormat()** 构造函数创建**国际号码。NumberFormat** 帮助格式化数字的对象。样式是十进制，所以数字是十进制格式的格式。

```
let amount = 6000000;
let k = new Intl.NumberFormat('en-US', {style: 'decimal'});
console.log(k.format(amount))
```

## java 描述语言

```
<script>

  // Javascript to illustrate Intl.NumberFormat constructor
  function func() {

    // Orignal Number
    let amount = 6000000;

    // Creating object to format Number
    let k = new Intl.NumberFormat("en-US", { style: "decimal" });

    // Formatting Number
    let l = k.format(amount);
    console.log(l);
  }
  func();
</script>
```

**输出:**

```
6,000,000
```

**例 7:** 在本例中，**国际机场。pluralrrules()**构造函数创建一个有助于复数敏感格式的对象。它返回一个字符串，该字符串指示用于数字的复数规则。

```
let l = new Intl.PluralRules().select(18);
console.log(l)
```

## java 描述语言

```
<script>

  // Javascript to illustrate
  // Intl.PluralRules constructor
  function func() {

    // Creating object for plural-sensitive
    // formatting of Number

    let l = new Intl.PluralRules();
    // selectign formatting for 18
    let k = l.select(18);
    console.log(k);
  }
  func();
</script>
```

**输出:**

```
other
```

**例 8:** 在本例中，**国际机场。RelativeTimeFormat()** 构造函数创建一个对象 Intl。相对时间格式有助于相对时间格式。它根据提供给构造函数的子标记进行格式化。

```
const relative = new Intl.RelativeTimeFormat('en', { style: 'narrow' });
console.log(relative.format(5, 'hours'));
```

## java 描述语言

```
<script>

// Javascript to illustrate Intl.RelativeTimeFormat constructor
function func(){

  // Creating object for formatting relative time
  const relative = new Intl.RelativeTimeFormat('en', { style: 'narrow' });

  // Formatting relative time for 5 value and hours unit
  let l =relative.format(5, 'hours');
  console.log(l)
}
func();
</script>
```

**输出:**

```
in 5 hr.
```