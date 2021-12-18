# JavaScript | generator . prototype . next()方法

> 原文:[https://www . geesforgeks . org/JavaScript-生成器-原型-下一个-方法/](https://www.geeksforgeeks.org/javascript-generator-prototype-next-method/)

**generator . prototype . next()**方法是 JavaScript 中的一个内置方法，用于返回一个具有两个属性 done 和值的对象。

**语法:**

```
gen.next( value );
```

**参数:**该功能接受如上所述的单个参数，描述如下:

*   **值:**该参数保存要发送给发电机的值。

**返回值:**这个方法返回一个包含两个属性的对象:

1.  **完成:**它有值
    *   **true**–对于迭代序列结束后的迭代器。
    *   **false**–对于能够产生序列中下一个值的迭代器。
2.  **值:**它包含迭代器返回的任何 JavaScript 值。

下面的例子说明了 JavaScript 中的 Generator.prototype.next()方法:

**例 1:**

```
function* GFG() { 
  yield "GeeksforGeeks";
  yield "JavaScript";
  yield "Generator.prototype.next()";
}

const geek = GFG(); 
console.log(geek.next());      
console.log(geek.next());      
console.log(geek.next());     
console.log(geek.next());  
```

**输出:**

```
Object { value: "GeeksforGeeks", done: false }
Object { value: "JavaScript", done: false }
Object { value: "Generator.prototype.next()", done: false }
Object { value: undefined, done: true }

```

**例 2:**

```
function* GFG(len, list) {
    let result = [];
    let val = 0;

    while (val < list.length) {
        result = [];
        let i = val
        while(i < val + len)
          {
            if (list[i]) {
                result.push(list[i]);
            }
           i+=1
        }

        yield result;
        val += len;
    }
}
list = [
    'geeks1','geeks2','geeks3',
    'geeks4','geeks5','geeks6',
    'geeks7','geeks8','geeks9',
    'geeks10','geeks11'
];

var geek = GFG(4, list);              

document.writeln(geek.next().value+"<br>");      
document.writeln(geek.next().value+"<br>");    
document.writeln(geek.next().value+"<br>");    
document.writeln(geek.next().value+"<br>");
```

**输出:**

```
geeks1,geeks2,geeks3,geeks4
geeks5,geeks6,geeks7,geeks8
geeks9,geeks10,geeks11
undefined
```

**支持的浏览器:**generator . prototype . next()方法支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   歌剧
*   旅行队
*   边缘