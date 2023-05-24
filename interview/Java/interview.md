# Java Core 复习问题

## Java Core

### Java Reference

[reference](https://cloud.tencent.com/developer/article/1657759)

### Java Arrays

1. 所有都是动态内存  
2. new了一个数组reference之后长度不可改变

### Java Set

1. hashSet底层是hashMap， 插入的元素是key

### Java HaspMap

1. 散列表，key-value映射
2. 最多允许一条记录的键为null
3. 无序的
[原理详解](https://zhuanlan.zhihu.com/p/127147909)

### Java List

1. OfferLast, Offer 和Add有什么区别
   1. offerlast和offer是一样的，offer出现是因为dequeue
   2. Add返回false只能因为已有元素，offerlast返回false是因为更多原因，失败了都是false



### class

1. interface 和class的区别.  
   1. interface是指接口，其中只有抽象方法，没有数据域，不能用其创建对象，可以继承其他接口，但是不能实现其他接口。 而class是指类，不能有抽象方法，可以有数据域，可以创建对象，可以实现接口，但不能继承接口。 class文件中只能包含一个类或者接口。  
   2. interface没有构造函数，class有构造函数
   3. interface不能进行运算重载
   4. interface的成员没有修饰符，总是公公的
   5. 派生于借口的类必须实现借口中所有成员的执行方式

### Generic

1. Type Parameter 和 Type Argument 区别
   1. type parameter是在定义generic，interface或methods使用的占位符类型
   2. `public class List<T>`就是type parameter
   3. type argument是实际创建时的data type
   4. `new List<String>`中string就是type argument
2. 创建泛型的实例时，jvm是会把具体类型擦除的；编译生成的字节码中不包含泛型中的类型参数，即`ArrayList<String>`和`ArrayList<Integer>`都擦除成了ArrayList，也就是被擦除成"原生类型"，这就是泛型擦除

## Java Unit Test
