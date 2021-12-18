# JavaScript | object . Getownpropertysdescriptors()方法

> 原文:[https://www . geeksforgeeks . org/JavaScript-object-getownpytimedescriptors-method/](https://www.geeksforgeeks.org/javascript-object-getownpropertydescriptors-method/)

JavaScript 中的**Object . GetownPropertyDescriptors()方法**是标准的内置对象，它返回给定对象的所有属性描述符。

**语法:**

```
Object.getOwnPropertyDescriptors( obj )
```

**参数:**该方法接受如上所述的单个参数，描述如下:

*   **obj:** 此参数保存要获取其所有属性描述符的对象。

**返回值:**该方法返回包含对象所有自身属性描述符的对象。对于没有属性的对象，此方法可能会返回一个空对象。

下面的例子说明了 JavaScript 中的 object . getowntpropertysdescriptors()方法:

**例 1:**

```
<script>
const geeks1 = {  
  prop1: "GeeksforGeeks" 
}  
const geeks2 = {  
  prop2: "Best Platform", 
  prop3: "And Computer science portal" 
} 
const descriptor1 = Object.getOwnPropertyDescriptors(geeks1);  
const descriptor2 = Object.getOwnPropertyDescriptors(geeks2);  
console.log(descriptor1.prop1.enumerable);  
console.log(descriptor2.prop2.enumerable);  
console.log(descriptor1.prop1.value);  
console.log(descriptor2.prop2.value); 
console.log(descriptor2.prop3.value); 
</script>
```

**输出:**

```
true
true
"GeeksforGeeks"
"Best Platform"
"And Computer science portal"
```

**例 2:**

```
<script>
const geeks1 = {  
  prop1: 22  
};  
const descriptors1 = 
    Object.getOwnPropertyDescriptors(geeks1);  

console.log(descriptors1.prop1.value);  
console.log(descriptors1.prop1);  
console.log(descriptors1.prop1.writable); 

const geeks2 = {  
  prop2: " getOwnPropertyDescriptors" 
};  

const descriptors2 = 
    Object.getOwnPropertyDescriptors(geeks2);  

console.log(descriptors2.prop2.writable);  
console.log(descriptors2.prop2.value);  
</script>
```

**输出:**

```
22
Object { value: 22, writable: true, enumerable: true, configurable: true }
true
true
" getOwnPropertyDescriptors"

```

**支持的浏览器:**object . getowntpropertysdescriptors()方法支持的浏览器如下:

*   谷歌 Chrome
*   火狐浏览器
*   工业管理学(Industrial Engineering)
*   歌剧
*   旅行队
*   边缘