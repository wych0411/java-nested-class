# Inner Class

> 一个类定义在另一个类内部，必须依附于一个Outer Class的实例。这是因为Inner Class除了有一个this指向它自己，还隐含地持有一个Outer Class实例，可以用Outer.this访问这个实力。所以，实例化一个Inner Class不能脱离Outer实例。

```java
class Outer {
  class Inner {
  	......
  }
}
```

> Outer Class被编译为Outer.class，而Inner Class被编译为Outer$Inner.class。
