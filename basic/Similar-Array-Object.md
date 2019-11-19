## 类数组对象

类数组对象 (Array-like Object) 是类似数组一样有length属性和索引属性的对象，其可以调用数组的某一些方法进行操作。如：

`const arrayLike = {a: 1, b:2, c: 3, length: 3}`

类数组对象应用`Array.isArray(arrayLike)`方法判断，返回值为`false`，因为其本质是对象并非数组

常见的类数组对象：

1. **函数的arguments**

2. **NodeList** 如`document.getElementsByTagName`、`document.querySelectorAll`、JQ的`$('.class')`等等获取`dom`的方法

3. **字符串String** 
    ```
    const array = Array.from('abc');
    console.log(array);
    //["a", "b", "c"]
    ```
