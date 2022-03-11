# java-nested-class

Java内部类

被定义在另一个类内部的类，被称为内部类（Nested Class）。

- ## Inner Class

> 定义在其它类内部的普通类。

- ## Anonymous Class

> 直接使用的没有类定义代码的匿名内部类。

- ## Static Nested Class

> 定义在其它类内部的用Static修饰的内部类。
---
Java的内部类克分为Inner Class、Anonymous Class和Static Nested Class三种：
- Inner Class和Anonymous Class本质上是相同的，都必须依附于Outer Class的实例，即隐含地持有Outer.this实例，并拥有Outer Class的private访问权限。
- Static Nested Class是独立类，但拥有Outer Class的private访问权限。
