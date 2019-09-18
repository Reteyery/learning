1. 属性

```java
    class Person {
        val name : String  // val 只读属性 等于 get
        var isMarried : Boolean // var 可写属性 等于 getter/setter
    }
```

2.自定义访问器

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

3.使用 when 处理枚举类等价于 case 

    when比case更强大，可以使用任意对象

4.
