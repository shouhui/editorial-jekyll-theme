# this指代的是谁
1. new关键字创建对象,构造函数里的this指代创建的新对象;
2. 显式绑定,函数内this指向使用call, apply, bind绑定的对象;
3. 隐式绑定,点操作符执行函数调用,函数内this指向点操作符前的对象
4. 默认绑定,非严格模式下为全局作用域,严格模式下为undefined

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
