# JavaScript 字符串 replaceAll()方法

> 原文:[https://www . geesforgeks . org/JavaScript-string-replace all-method/](https://www.geeksforgeeks.org/javascript-string-replaceall-method/)

下面是字符串替换方法的一个例子。

## java 描述语言

```
<script>
function gfg() {
    let string = "Geeks or Geeks";
    newString = string.replaceAll("or", "for");
    document.write(newString);
}
gfg();
</script>
```

**输出:**

```
Geeks for Geeks
```

**replaceAll()** 方法在用指定字符串或正则表达式替换字符串的所有匹配项后，返回一个新字符串。

执行此操作后，原始字符串保持不变。

**语法:**

> const newString = originalstring . replace all(regexp | substr，newSubstr | function)

**参数:**该方法接受以下定义的某些参数:

*   **regexp:** 是用 newSubstr 或指定函数返回的值替换匹配项的正则表达式。
*   **substr:** 定义要用 newSubstr 或指定函数返回的值替换的子字符串。
*   **newSubstr:** 它是替换子字符串或正则表达式指定的字符串的所有匹配项的子字符串。
*   **函数**:调用该函数，用 regexp 或 substr 替换匹配项。

#### 例 1:

## java 描述语言

```
<script>
function GFG() {
    let string = "Hello, what are you doing?";
    newString = string.replaceAll("Hello", "Hi");
    document.write(newString);
}
GFG();
</script>
```

#### 输出:

```
Hi, what are you doing?
```

#### 例 2:

## java 描述语言

```
<script>
function GFG() {
    const regexp = /coffee/ig;
    let string = "Lets, have coffee today!";
    newString = string.replaceAll(regexp, "tea");
    document.write(newString);
}
GFG();
</script>
```

**输出:**

```
Lets, have tea today!
```

**支持的浏览器:**

*   Chrome 85 及以上
*   边缘 85 及以上
*   Firefox 77 及以上版本
*   歌剧 71 及以上
*   Safari 13.1 及以上版本