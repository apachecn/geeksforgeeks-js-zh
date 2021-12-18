# JavaScript URIError |格式错误的 URI 序列

> 原文:[https://www . geesforgeks . org/JavaScript-uri error-畸形-uri-sequence/](https://www.geeksforgeeks.org/javascript-urierror-malformed-uri-sequence/)

如果对 URI 的编码或解码不成功，就会出现这种 JavaScript 异常**格式错误的 URI 序列**。

**消息:**T0】

**错误类型:**

```
URIError

```

**错误原因:**该错误在代码中的某个地方抛出，URI 编码或解码不成功。

**示例 1:** 在此示例中，传递的值不可接受，因此出现了错误。

## HTML

```
<script>
  // Error here
  encodeURI('\uD810');
</script>
```

**输出:**

```
URIError: URI malformed
```

**示例 2:** 在此示例中，传递的值不可接受，因此出现了错误。

## HTML

```
<script>
  // Error here
  decodeURIComponent('%E0%B4%A'); 
</script>
```

**输出:**

```
URIError: URI malformed
```