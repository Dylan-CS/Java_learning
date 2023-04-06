# 1 Java SE foundaton

## 1. java语言初识

### MarkDown语法

###  简单的Dos命令

### 计算机语言发展史

### java的诞生

- 1995年

	- JAVA SE
	- JAVA ME（手机端）

		- Android

	- JAVA EE

- 2006年

	- Hadoop（大数据系列）

### JDK

- 开发者工具包

### JRE

- 运行环境

## 2. HelloWorld

### public class Hello{}

public class Hello{
	public static void main(Stringp[ args){
		System.out.println("Hello World");
	}
}

- javac Hello.java

	- 生成class文件

- java Hello
- 编译型语言
- 解释型语言
- IDEA

## 3. 基础语法

### 注释

- 行内注释//
- 多行注释/**/
- 文档注释/** */

	- javadoc 生成帮助文档

### 标识符

- 关键字

### 数据类型

- 基本数据类型

	- 整数

		- byte 1
		- short 2
		- int（默认）4
		- long 8
		- 0b 二进制
		- 0o 八进制
		- 0x 十六进制

	- 浮点数

		- float 4
		- double（默认）8
		- BigDecimal

	- 字符

		- char 2
		- asscii
		- utf-8
		- Unicode
		- ‘\u0000’

			- \b 退格
			- \n 换行
			- \r 回车
			- \t 制表
			- \'
			- \''
			- \\

	- 布尔值

		- boolean 1
		- if(a)

- 引用数据类型

	- 类
	- 接口
	- 数组

### 类型转换

- 自动类型转换

	- 低转高

- 强制类型转换

	- 高转低（高）低

### 变量和常量

- type varName [=value];
- 作用域

	- 类变量
	- 实例变量
	- 局部变量

- 常量

	- final MAX_A = 10;

- 命名规范

	- 1.见名知意
	- 2.驼峰命名（变量、方法）
	- 3.类、首字母大写，驼峰命名
	- 4.常量：大写+下划线
	- 5.不要使用拼音命名

### 运算符

- 算术运算符

	- +  -  *  %  /

- 赋值运算符

	- =

- 关系运算符

	- >  <  >=  <=  ==  !=  instanceof(用来判断其左边对象是否为其右边类的实例)

- 逻辑运算符

	- && || ！

- 位运算符

	- & | ^ ~ >> << >>>

- 条件运算符

	- ? :

- 扩展运算符

	- +=   -=   *=  /=

### 包机制

- 域名倒写
- 作用：防止命名冲突
- package
- import

### javaDoc

- JDK帮助文档
- 1.javadoc

	- @author
	- @Version
	- @Since
	- @param
	- @return
	- @throws

## 4.流程控制

### Scanner

- 用户交互 System.in

### 顺序结构

- 程序默认的结构，自上而下的执行

### 选择结构

- if 单选择结构
- if-else 双选择结构
- if-else if - else 多选择结构
- switch

	- jdk 支持了String类型
	- case 穿透现象
	- default

### 循环结构

- while

	- 尽量避免死循环

- do...while
- for

	- for（int i=0;i<100;i++）

- for-each 增强for循环

### break & contiune

- break：跳出循环
- 带标签break
- continue：终止当次循环
- 带标签continue
- return：结束方法的运行

## 5.方法

### 什么是方法！

- 语句块的集合

### 方法的定义

- 修饰符 方法名（参数名）{
return 返回值；
}

### 方法调用

- 类名.方法
- 对象.方法

### 方法重载

- 名字相同，参数列表不同

### 命令行传参

- 给main方法传递参数

### 可变长参数

- ...
- 必须放在最后一个参数

### 递归

- 自己调用自己，给自己一个出口
- 面试常问

## 6.数组

### 数组的定义

- new int[5]
- {1，2，3，4，5}

### 数组的使用

- 通过下标拿到值
- ArrayindexoutofBounds
- 增强for循环遍历

### 二维数组

- int[ ][ ]

### Arrays 工具类

### 排序算法

- 冒泡排序
- 选择排序
- 插入排序
- 快速排序
- 归并排序
- 希尔排序
- 堆排序
- 基数排序

## 7.面向对象

### 类与对象

- 类是对象的抽象：模板Class
- 对象是类的具体

### 构造方法

- 构造的重载

	- 默认的无参构造
	- 如果手动定义了有参构造就必须手动再加一个无参构造
	- 单例模式，需要构造器私有！

### new对象

- 栈存放引用
- 堆存放具体的对象

### 封装

- 属性私有，提供对应的get、set

### 继承

- extends
- Object
- 子类拥有父类的全部特性
- 方法重写
- this
- super
- java是单继承，之能继承一个父类

### 多态

- 父类的引用指向子类的对象 Person person = new Student（）；
- instanceof 关键，如果匹配，可以进行类型之间的转换

### 修饰符

- public
- protect
- private
- static
- final
- abstract

### 接口

- interface
- 约束，只能定义方法名
- 子类实现接口，必须重写其中的方法
- 只有一个方法的接口叫做函数式接口，可以使用lambda表达式简化
- 接口比抽象类更抽象
- 一个类可以实现多个接口

### 内部类

- 局部内部类
- 静态内部类
- 匿名内部类（重点）

## 8.异常

### Throwable

- Exception

	- 运行时异常

		- 1/0
		- NullPoint
		- UnKnownType
		- 下标越界异常
		- ......

	- 检查型异常

- Error

	- AWT错误
	- JVM错误

		- StackOverFlow
		- OutOfMemory

### 五个关键字

- try{}
- catch（）{}

	- 先小后大

- finally{}
- throw

	- 手动抛出异常

- throws

	- 方法抛出异常

### 自定义异常

- 继承Exception类即可

## 9.常用类

### Object类

- Hashcode（）
- toString（）
- Clone（）
- getClass（）
- notify（）
- wait（）
- equals（）

### Math类

- 常见的数学运算

### Random类

- 生成随机数

	- UUID

### File类

- 创建文件
- 查看文件
- 修改文件
- 删除文件

### 包装类

- 自动装箱和拆箱

### Date类

- Date
- SimpleDateFormat

	- yyyy-MM-dd HH：mm：ss

- Calendar（建议使用）

### String类

- 不可变性

	- final

		- 因为String太常用了，设置为不可变的是为了减少大量的同步锁的开销

### StringBuffer

- 可变长

	- append（）

		- 多线程数据量较大

			- 效率低，安全

### StringBuilder

- 可变长

	- 单线程数据量较大

		- 效率高，不安全

## 10.集合框架

### Collection

- List 有序可重复

	- ArrayList 常用

		- add
		- remove
		- contains
		- size

	- LinkedList 常用

		- getFirst（）
		- getLast()
		- removeFirst()
		- addFirst()

	- Vector
	- Stack

- Set 无序不可重复

	- HashSet 常用
	- TreeSet

### Map

- HashMap 很常用

	- JDK 1.7 数组＋链表
	- JDK 1.8 数组＋链表+红黑树

- TreeMap

### Collections 工具类

### 泛型<> 约束，避免类型转换之间的问题

## 11.IO流

### 字节流

- 输入：InputStream
- 输出：OutputStream

### 字符流

- Reader
- Writer

### 节点流

- CharArrayReader、Wirter、inputStream、outputStream
- StringReader、writer
- pipe（管道流）
- File（，，，）

### 处理流

- buffer

	- bufferInputStream
	- bufferOutputStream
	- bufferReader
	- bufferWriter

- 序列化

	- 反序列化

		- Serializable

			- transient

- data

	- DataInputStream
	- DataOutputStream

- object流
- 转换流

	- InputStreanReader
	- OutputStreamWriter

- Filter

	- 四个

- print

	- PrintWriter
	- PrintStream

## 12.literator 迭代器

## 13.静态代理

### new Thread（Runnable).start();

## 14.lambda表达式

### 函数式编程

### 避免内部类定义过多

### new Thread（（）->{
System.out.println();
}).start();

## 15.多线程

### 进程和线程

### run（），Start（）

### 线程创建的方式

- Thread

	- start0，本地方法：java无权调用，交给底层C处理

		- private natie void start0（）；

- Runnable

	- 函数式接口

		- lambda

- Callable

	- 可以有返回值

### 静态代理

- new Thread（Runnable).start();

### lambda表达式

- 函数式编程
- 避免内部类定义过多
- new Thread（（）->{
System.out.println();
}).start();

### 线程的状态

- 新建状态
- 就绪
- 运行
- 阻塞
- 死亡

### 常用的方法

- sleep
- join
- yleid
- isLive
- start
- setPriority
- interrupt

### 线程同步

- 多个对象操作同一个资源，并发
- 前提：队列+锁
- Synchronized

	- 同步方法

		- 弊端：锁太多了

	- 同步代码块 常用
	- 第一个线程进来拿到锁，后面就要排队了，直到这个人释放锁，后面拿到锁才能进去
	- 死锁：两个人都抱着对方的锁

		- 互斥
		- 请求与保持
		- 不剥夺条件
		- 循环等待条件

- Lock（优先级高）

	- ReentrantLock

		- lock
		- trylock
		- unlock

### 线程通信

- 缓冲区：消息队列
- 标志位：红绿灯
- wait（）；
- notifyAll（）；

### 线程池（Pool）

- 池化技术
- 池的大小
- 最大连接数
- 保持时间
- 。。。。。

## 16.网络编程

### IP

### 端口

### Socket编程

### TCP

- 三次握手
- 四次挥手

### UDP

- 无连接
- Packet

### URL

### 初识Tomcat

### 聊天通信

### 文件上传

## 17.GUI（可选）

### AWT

- Frame
- 监听事件

	- 鼠标
	- 键盘
	- 窗口
	- 文本框
	- 动作事件

### Swing

- 文本框
- 标签
- 按钮
- 文本域
- 面板
- 布局方式
- 关闭窗口
- 列表

### 贪吃蛇

- Timer
- 键盘监听
- 游戏帧的概念

## 18.注解和反射

### 注解

- 元注解
- 内置注解
- 自定义注解
- 反射读取注解

### 反射

- Class

	- newinstance（）；

- 类加载机制
- Method

	- invoke（user3，“qinjiang3”）；
	- 存在重载，也需要参数的类型

- Field

	- set（user4，“qinjiang4”）；

- Construct

	- newInstance（）；
	- 获取的时候需要传递参数的class类型

- 破坏私有的关键字

	- setAccessible（true）；

- 性能分析

	- 正常>检测关闭的反射》默认的反射

- 反射获得注解，泛型...

### 单例模式的探究

### Stream

### Forkjoin

- 效率对比

*XMind: ZEN - Trial Version*