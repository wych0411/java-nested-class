# Static Nested Class

> Static Nested Class与Inner Class类似，但是使用static修饰，称为静态内部类。

```java
class Outer {

  static class StaticNested {
  	......
  }
}
```
用static修饰的内部类和Inner Class有很大的不同，它不再依附于Outer的实例，而是一个完全独立的类，因此无法饮用Outer.this，但它可以访问Outer的private静态字段和静态方法。如果把Static Nested移到Outer之外，就失去了访问private的权限。
