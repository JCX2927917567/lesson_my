- git log
    由于提交记录过多，自动进入到vi 的编辑状态
    j 代表上移
    k 下移
    q 退出
    o 新行
    i 编辑

- 变量提升和暂时性死区
    编译阶段 早于运行阶段
    var          let (不可以在声明前使用，暂时性死区)  走两条路
    js 语言的特点，在代码运行前确立作用域
    所有的变量都是属于作用域管理的
    js 里面的变量，是有作用域的VO {name}
    变量提升 不好的

- this 终极话术
    this 永远指向最后调用它的那个对象

- this 
    函数运行时创建的一个指针    指向谁?
    1. 指向是不固定的，运行的方式来决定
    2. add作为普通函数被调用时，this指向？
        没有被谁调用，返回值就是 运行环境
        window
        严格模式  undefined

    3. 作为对象方法调用时，this指向对象
    4. 函数作为构造函数使用时，this指向实例
    5. 函数作为事件的回调函数来执行的时候指向事件方式的元素

- 严格模式
    js 语言早期 开发的很快 存在语言的糟粕 如何避开他？
    - 普通函数运行时 this 指向全局
    - 定义变量时 什么也不用（var,let const）， 全局变量

- 作用域
    1. 全局
    2. 函数
    3. 块级(es6 + let const)
    变量一定会属于某个作用域

- this指向谁? 最后由谁调用
    1. 普通函数     window
    2. 严格模式     undefined
    3. 对象的方法   对象
    4. new          实例
    5. 事件处理函数  事件发生的对象

- 如何指向this
    6. call apply 手动指定this 指向第一个参数
        借用方法  除了指定this还可以传参
        call 展开来     apply[]
    7. bind 返回一个被指定了this的函数
        未来被调用时 this 指向那个对象
    8. that = this 作用域链 专业前端
    9. 箭头函数 内部没有this 找到外层的this