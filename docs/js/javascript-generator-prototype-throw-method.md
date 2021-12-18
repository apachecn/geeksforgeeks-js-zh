# JavaScript | generator . prototype . throw()方法

> 原文:[https://www . geesforgeks . org/JavaScript-生成器-原型-抛出-方法/](https://www.geeksforgeeks.org/javascript-generator-prototype-throw-method/)

**generator . prototype . throw()**方法是 JavaScript 中的一个内置方法，用于通过向生成器中抛出一个错误来恢复生成器的执行。
**语法:**

```
gen.throw(exception);
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **异常:**此参数保存要抛出的异常。

**返回值:**这个方法返回一个包含两个属性的对象:

1.  **完成:**它有值
    *   **true**–对于迭代序列结束后的迭代器。
    *   **false**–对于能够产生序列中下一个值的迭代器。
2.  **值:**它包含迭代器返回的任何 JavaScript 值。

以下示例说明了 Generator.prototype.throw()方法，如下所示:
**示例 1:**

## java 描述语言

```
<script>
function* GFG() {
  while(true) {
    try {
       yield "Null";
    } catch(e) {
      console.log('Generator.prototype.throw()');
    }
  }
}

const geeks = GFG();
console.log(geeks.next());
console.log(geeks.throw(new Error('Error caught!')));      
</script>  
```

**输出:**

```
Object { value: "Null", done: false }
"Generator.prototype.throw()"
Object { value: "Null", done: false }
```

**例 2:**

## java 描述语言

```
<script>
function* GFG(pageSize = 1, list) {
    let output = [];
    let index = 0;

    while (index < list.length) {
      try {
        output = [];
        for (let i = index; i < index + pageSize; i++) {
            if (list[i]) {
                output.push(list[i]);
            }
        }

        yield output;
        index += pageSize;
      } catch(e) {
      console.log('Generator.prototype.throw()');
    }
    }
}
list = [1, 2, 3, 4, 5, 6, 7, 8]
var geek = GFG(3, list);             

console.log(geek.next());     
console.log(geek.next());     
console.log(geek.next());
console.log(geek.throw(new Error('Error caught!')));
</script>
```

**输出:**

```
Object { value: Array [1, 2, 3], done: false }
Object { value: Array [4, 5, 6], done: false }
Object { value: Array [7, 8], done: false }
"Generator.prototype.throw()"
Object { value: Array [7, 8], done: false }
```

**支持的浏览器:**generator . prototype . throw()方法支持的浏览器如下:

*   谷歌 Chrome 39 及以上
*   Firefox 26 及以上版本
*   歌剧 26 及以上
*   Safari 10 及以上
*   边缘 13 及以上