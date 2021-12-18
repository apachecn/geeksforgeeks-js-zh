# 运算符

中的 JavaScript

> 原文:[https://www.geeksforgeeks.org/javascript-in-operator/](https://www.geeksforgeeks.org/javascript-in-operator/)

下面是操作符中**的例子。**

*   **例 1:**

    ```
    <script> 
        function gfg() { 
        // Illustration of in operator
        const array = ['geeks', 'for', 
                       'geeks']

        // Output of the indexed number
        document.write(0 in array);  

        // Output of the Value
        document.write('for' in array);

        // output of the Array property
        document.write('length' in array);
        } 
        gfg(); 
    </script>
    ```

*   **输出:**

    ```
    true
    false
    true
    ```

运算符中的**是 JavaScript 中的内置运算符，用于检查对象中是否存在特定属性。如果指定的属性在对象中，则返回布尔值*真*，否则返回*假*。**

**语法:**

```
prop ***in*** object

```

**参数:**该功能接受如下参数，如上所述，如下所述:

*   **道具** ***:*** 此参数保存代表属性名或数组索引的字符串或符号。
*   **对象:**该参数是要检查是否包含*道具的对象。*

**返回值:**该方法返回一个布尔值:

*   **真:**如果指定的属性是在对象中找到的*，则返回值*真***。***
*   ****false:** 如果在对象中未找到指定属性*，则返回值*false***。*****

*****以下示例说明了 JavaScript 中运算符中的**:*******

*******例 1:*******

```
***<script>
    // Illustration of in operator
    const array = ['geeksforgeeks', 'geeksfor', 
                   'geeks', 'geeks1']

    // Output of the indexed number
    console.log(0 in array)        
    console.log(2 in array)       
    console.log(5 in array)       

    // Output of the Value
    console.log('for' in array)
    console.log('geeksforgeeks' in array)

    // output of the Array property
    console.log('length' in array)
</script>***
```

*******输出:*******

```
***> true
> true
> false
> false
> false
> true*** 
```

*******例 2:*******

```
***<script>
    // Illustration of in operator
    const object = { val1: 'Geeksforgeeks', 
                     val2: 'Javascript',
                     val3: 'operator', 
                     val4: 'in' };

    console.log('val1' in object);

    delete object.val1;
    console.log('val1' in object);

    if ('val1' in object === false) {
      object.val1 = 'GEEKSFORGEEKS';
    }

    console.log(object.val1);
</script>***
```

*******输出:*******

```
***> true
> false
> "GEEKSFORGEEKS"*** 
```

*******支持的浏览器:**操作符中的 JavaScript **支持的浏览器如下:*******

*   *****谷歌 Chrome*****
*   *****火狐浏览器*****
*   *****歌剧*****
*   *****旅行队*****
*   *****边缘*****
*   *****微软公司出品的 web 浏览器*****