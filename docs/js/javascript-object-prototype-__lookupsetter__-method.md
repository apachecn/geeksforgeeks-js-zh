# JavaScript object . prototype . _ _ lookback ter _ _()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-object-prototype-_ _ lookbackter _ _-method/](https://www.geeksforgeeks.org/javascript-object-prototype-__lookupsetter__-method/)

JavaScript*Object . prototype . _ _ LookOundter _ _()*方法用于在为对象的属性定义 Setter 函数时获取对该函数的引用。无法通过该属性引用 setter 函数，因为它引用了函数的返回值。它返回作为 setter 绑定到指定属性的函数。

**语法:**

> o . prototype . _ _ look back ter _ _(P)

**术语:**

*   **O:** 指对象(此值)。对象接受参数值。它将参数转换为对象值。
*   **P :** 指从属性(P)生成的字符串键。它指的是应该由 setter 返回的属性的名称。

**返回值:**

*   If object O is empty or IsAccessorDescriptor is *false* , undefined is returned.
*   If the object O is not empty, and the IsAccessorDescriptor is *true* , the function bound to the specified property as a setter is returned.

**示例 1:** 它返回一个名为 *gfg()* 的函数。

## Javascript

```
<script>
const gfgObject = {
  set gfg(arg) {
    this.portalName = arg;
    console.log(portalName)
  }
};

const gfgFunction = gfgObject.__lookupSetter__('gfg')
gfgFunction("GeeksforGeeks");
</script>
```

**输出:**

```
GeeksforGeeks
```

Web 标准不再推荐此功能。虽然它仍然受到一些浏览器的支持，比如谷歌 Chrome，但它正在被淘汰。它不应该用于任何新的或旧的项目。依赖它的页面或网络应用程序随时都有可能失败。

建议使用*object . getowntpropertysdescriptor()。设置*，取两个参数。

*   Who should look for property.
*   The name of the property from which to retrieve the description.

**注意:**返回作为属性设置器的函数，如果没有设置器则返回*未定义的*。

**例二:**

## Javascript

```
<script>
const gfgObject = {
  set gfg(arg) {
    this.portalName = arg;
    console.log(portalName)
  }
};
const gfgFunction =  
  Object.getOwnPropertyDescriptor(gfgObject,"gfg").set
gfgFunction("GeeksforGeeks");
</script>
```

**输出:**

```
GeeksforGeeks
```

**支持的浏览器:**

*   Google Chrome
*   Internet browser
*   red fox

**注意:**此功能已被弃用，不再推荐。