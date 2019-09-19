1. 属性

```java
    class Person {
        val name : String  // val 只读属性 等于 get
        var isMarried : Boolean // var 可写属性 等于 getter/setter
    }
```
2. 自定义访问器

```java
    class Retangle(val height : Int, val width : Int){
        // 声明getter属性
        val isSquare : Boolean
            get() {
                return height == width
            }
        //等价于 get() = height == width
    }
```
3. 使用 when 处理枚举类等价于 case 

    when比case更强大，可以使用任意对象
4. 创建集合

```java
    val set = hashSetOf(1, 7, 53)
    val list = arrayListOf(1, 7, 53)
    val map = hashMapOf(1 to "one", 7 to "seven", 53 to "fifty-three")
```
5. 消除静态工具类：顶层函数和属性

6. 扩展函数和属性

    扩展函数在java中将会被编译成 static method；当给基类和子类都定义一个同名的扩展函数，输出结果由该变量的静态类型所决定，而不是这个变量的运行时类型
    eg:
```java
    fun View.showOff() = println("I'm a view")
    fun Button.showOff() = println("I'm a button")
>>> val view: View = Button()
>>> view.showOff()
I'm a view 
```
    以下例子扩展String属性，增加lastChar函数功能，this代表String类型的一个实例，即字符串"Kotlin"
```
    package com.rete.kotlin

    fun String.lastChar(): Char = this.get(this.length - 1)

    fun main(args : Array<String>) {
        println("Kotlin".lastChar())
    }
```
7. 处理集合：可变参数、中缀调用

    解构声明，用来把一个单独的组合值展开到多个变量中
8. 