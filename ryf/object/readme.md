# 一起读技术文章，提升我们的认知

1. c 语言 工程式 函数 main()
    js 基于(面向)对象？
    面向?   基于?
    object-base

2. js原来没有class关键字
    var es5     let const es6以后
    es6才有class关键字
    js 不是一种真正的面向对象语言，是基于对象的语言，这个对象是Object，所有对象的原型都是Object

3. js中除了简单数据类型都是对象
    任何一个对象都有一个_proto_私有属性去说明他基于哪个对象创建的

4. js 本没有类，早期class关键字没有
    但是内置了一个object对象
    其他对象都基于这个对象进行创建
    再把这个对象的构建过程(属性和方法集合)，用一个函数来封装
    new  Person() 得到了 基于对象的新对象

5. 基于对象，生成实例对象的原始模式 一步步创建的
    缺点是慢，重复

6. 函数封装对象
    缺点是  不能反映出它们是同一个原型对象的实例

7. js使用构造函数的方式来创建类
    以new的方式来运行
    对象构建过程的封装 this指向实例
    另外 class 有的 instanceof 也有
    并且兄弟对象之间基于的对象一致

8. js 基于对象
    - _proto_   Object
    - instanceof 

9. js 中创建类 写个构造函数

10. js如何构建类的
    - 类就是属性和方法的集合，抽象的
    - 先使用构造函数 定义实例属性的构造过程，每个对象属性是不一样的，
        归实例自己所有 this
    - 由于 实例共有的属性和方法，没必要放在构造函数内，会消耗不必要的内存
    - 每个函数都有一个prototype 属性，专门用来设计共享的属性或方法对象
        原型对象
        js 类 = 构造函数(condtructor) + prototype
        new 构造函数(constructor)       实例对象
    - 实例是怎么拿到构造函数的prototype里的属性或方法
        -proto
