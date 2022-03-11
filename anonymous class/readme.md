# Anonymous Class

> 匿名内部类，与普通内部类的区别在于不存在类定义代码，只是在需要的时候直接new出，因为没有定义类名，因此称为匿名。

1.匿名内部类的使用场景比较常见的是线程的新建：
```
class Outer {

  	private String name;

  	public Outer(String name) {
  		this.name = name;
  	}

  	void asyncHello() {
  		Runnable r = new Runnable() {

  			@Override
  			public void run() {
  				System.out.println("Hello," + Outer.this.name);
  			}
  		};

  		new Thread(r).start();
  }
}
```

2.除了接口外，匿名类也可以继承自普通类。
```
HashMap<String, String> map = new HashMap<>() {};
HashMap<String, String> map2 = new HashMap<>() {
 {
  put("A", "1");
  put("B", "2");
 }
};
System.out.println(map2.get("A"));
//map是一个匿名类实例，只是该匿名类继承自HashMap。
//map2也是一个继承自HashMap的匿名实例，并且添加了全局代码块来初始化数据。
```

匿名内部类和Inner Class一样，可以访问Outer Class的private字段和方法。

之所以要定义匿名类，是因为在定义的位置通常不关心类名，比直接定义Inner Class可以少写很多代码

Outer Class被编译为Outer.class，而Anonymous Class被编译为Outer&1.class。如果有多个匿名类，Java编译器会将每个匿名类依次命名为Outer$1、Outer$2、Outer$3......
