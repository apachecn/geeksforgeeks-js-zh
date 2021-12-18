# 如何在 JavaScript 中对一个累加器和对象的每个键应用函数？

> 原文:[https://www . geeksforgeeks . org/如何针对 javascript 中的累加器和对象的每个键应用函数/](https://www.geeksforgeeks.org/how-to-apply-function-against-an-accumulator-and-each-key-of-object-in-javascript/)

在本文中，我们将看到如何在 JavaScript 中针对累加器和对象中的每个键应用函数。累加器可以是函数、对象、数组等。在本文中，我们使用一个对象的累加器和键来对抗函数。

**进场:**在我们的进场中，我们使用减少。首先，我们从对象中获取密钥并创建一个函数。获取键后，我们使用 reduce 对键和累加器的集合应用函数。在简化方法中，我们使用累加器和键作为回调函数的参数，回调函数是我们的函数。

**语法:**

```
Collection.reduce((accumulator, key)=>
    function(accumulator,key), InitialValue);
```

**例 1:**

## java 描述语言

```
<script>
    function ApplyingFn() {

        // Function that apply against accumulator
        function function(robj, key) {

            // Limits for salary for persons
            var l1 = 'Below 30000';
            var l2 = 'Below 40000';
            var l3 = 'Below 50000';
            var l4 = 'Above 50000';

            // Checking salary of persons
            if (m[key] < 30000) {

                // Creating group for same
                // salary below Limits
                robj[l1].push(key);
            }
            if (m[key] < 40000) {

                // Creating group for same
                // salary below Limits
                robj[l2].push(key)
            }
            if (m[key] < 50000) {

                // Creating group for same
                // salary below Limits
                robj[l3].push(key)
            }
            else {

                // Creating group for same
                // salary below Limits
                robj[l4].push(key)
            }
            return robj;
        }

        // object for the salary
        var k = {
            'Below 30000': [], 'Below 40000': [],
            'Below 50000': [], 'Above 50000': []
        };

        var m = {
            'Rahul': 15000, 'Shyam': 220000,
            'David': 420000, 'Sam': 35000, 'Ram': 450000
        };

        // Apply Function against accumulator
        // and key of object
        var l = Object.keys(m).reduce((accumulator,
            key) => function(accumulator, key), k);
        console.log(l);
    }
    ApplyingFn();
</script>
```

**输出:**

```
{'Below 30000': ['Rahul'],

'Below 40000': ['Rahul', 'Sam'],

'Below 50000': ['Rahul', 'Sam'],

'Above 50000': ['Shyam', 'David','Ram']}
```

**例 2:**

## java 描述语言

```
<script>
    function ApplyingFn() {

        // Function which is applied
        // against accumulator
        function function(robj, value, key) {

            // Checking key is first or not
            if (robj[value] == undefined) {

                // Creating group for same key
                robj[value] = [];
                robj[value].push(key);
            }

            // If key is already taken
            else {

                // Inserting value in grounp
                robj[value].push(key)
            }

            return robj;

        }
        var m = {
            'Ms.Dhoni': 'Cricket',
            'Sunil Chhetri': 'Football',
            'Rishabh Pant': 'Cricket',
            'K.L Rahul': 'Cricket',
            'Ishan Pandita': 'Football',
        };

        // Apply Function against accumulator
        // and key of object
        var l = Object.keys(m).reduce((accumulator,
            key) => function(accumulator, m[key], key), {});
        console.log(l);
    }
    ApplyingFn();
</script>
```

**输出:**

```
{'Cricket': ['Ms.Dhoni', 'Rishabh Pant', 'K.L Rahul'],
'Football': ['Sunil Chhetri', 'Ishan Pandita']}
```