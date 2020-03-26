# 关于js类型的几个问题
1. 为何有的编程规范要求使用void 0代替undefined
undefined不是js的关键字,只是内部定义的全局对象的属性,es5(包含)后该变量不能配置和赋值,但是可以在非全局作用域覆盖定义同名undefined变量
例如:
```
    <script>
        function print() {
            'use strict'
            var undefined = 4;
            console.log(undefined); //  4
        }
        print();
    </script>
```
2. 小数 0.1 + 0.2 是否等于0.3
不相等,小数计算有精度误差

3. js是面向对象语言,还是基于对象语言
