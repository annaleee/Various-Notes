# Javascript

## hoisting

js的一种机制，将声明的变量提前储存，供后续操作。function可以写在后面，但是提前使用var的变量只能得到undefined。  
函数的提升优先级始终高于普通变量

## promise

promise创建时，会传给exutor，excutor含有resolve和reject。在promise创建时，excutor会立刻执行。创建时的promise内部是个对象，初始为state和result。一旦excutor执行完，要么产生value，要么产生error。当产生value时，会立刻调用resolve，当产生error时，会立刻调用reject。  
then: 传入result和error开始操作  
catch: 捕获整个异步操作的错误
finally: 清理操作
fetch: 这个方法用来发起网络请求

## callback

把函数当作参数传给函数

## var/let/const

1. var: 局部作用域变量（全局或者函数内部
2. let: 块级作用域变量（花括号
3. const: 常量（花括号

## prototype

因为js没有class，所以用constructor和prototype来弥补。  
构造函数名首字母必须大写，内部使用this对象  
同一个构造函数的对象实例无法共享属性或者方法  
如果是class.prototype.hobby = function(){},就可以解决这个问题。  
这个回家仔细看

## array有哪些函数

1. push: 在数组末尾添加一个或者多个元素
2. delete: 头部添加一个或者多个元素
3. pop:删除最后一个元素
4. shift:删除数组的第一个元素
5. join:把所有元素都转化为字符串拼在一起，可以指定分隔符
6. reverse: 返回逆序数组
7. sort:排序,第一个参数是function
8. concat: 返回新数组
9. slice: 返回数组切片
10. splice: 返回删除了元素以后的数组
11. toString: 输出了用逗号分隔的字符串列表
12. forEach: abc，从头到尾遍历数组，修改本数组
13. map: 将调用的函数每个元素传递指定的函数，返回一个数组
14. filter
15. every: 当且仅当所有的元素调用都是true，才会返回true
16. some: 只要有一个是true，那就会返回true
17. reduce: 组合生成单个值
18. flat: 搞平
