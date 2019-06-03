## JS知识点

[1、null和undefined的区别](#null和undefined的区别)

[2、类数组对象](#类数组对象)

1. ### null和undefined的区别

    `null`是一个表示"无"的对象，转为数值时为0；`undefined`是一个表示"无"的原始值，转为数值时为`NaN`。

    当声明的变量还未被初始化时，变量的默认值为`undefined`。

    `null`用来表示尚未存在的对象，常用来表示函数企图返回一个不存在的对象。

    `undefined`表示"缺少值"，就是此处应该有一个值，但是还没有定义。典型用法是：

    （1）变量被声明了，但没有赋值时，就等于`undefined`。

    （2) 调用函数时，应该提供的参数没有提供，该参数等于`undefined`。

    （3）对象没有赋值的属性，该属性的值为`undefined`。

    （4）函数没有返回值时，默认返回`undefined`。

    `null`表示"没有对象"，即该处不应该有值。典型用法是：

    （1） 作为函数的参数，表示该函数的参数不是对象。

    （2） 作为对象原型链的终点。

2. ### 类数组对象

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
