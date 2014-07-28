kenny-s_cloud_language
======================

原则：

1.语言级的回调
2.任意方法执行创建多线程，执行完毕回调
3.动态执行的代码和编译器编译的一模一样，运行期的编译器，代码在内存中的组织，管理
4.线程间传递数据都是拷贝（分清楚拷贝 和 共享资源|引用）
5.如果可以优化性能，这样做：读取时都是引用，写的时候，才在自己线程开辟空间，拷贝一份，再写，涉及线程以及他自己的内存空间的管理组织
6.一切数据都是容器，统一容器；数据其实是对象运行所需要的资源。
7.方法执行时才实例化对象，其实是实例化线程，轻量级线程虚拟机
8.类就是对输入数据的格式进行规范，接口就是对输入和输出都进行规范的类，任何类都隐含是接口（接口和类的统一）
9.继承就是在类创建的时候把父母类的所有东西都拷贝一份，加工结合，至于以后就跟父母类没有关系了，这就像是基因。（程序员就是造物主，决定怎么结合）
10.运行时对一切方法，变量的查找，支持正则，迫使程序员关注命名问题
11.数据其实是树结构，线程创建也是树结构，对树要有抽象的操作，比如层级查找统计，簇查找统计。list是特殊的map，map是特殊的树
12.有管理的哲学意识，任何东西都要可管理，可监控（）
13.数据像水一样流动（支持转化，过滤，添加），对象像人一样繁殖（第9条）
14.所有基本类型只有字符串，数字，二进制；字符串是特殊的二进制


哲学：
1.
类比的能力，所有动物，都有嘴，可以吃饭，有消化系统，神经系统，呼吸系统，都有，但是各物种之间有细微的差别，以适应各自不同的环境
从时间的角度，是一个祖先，经过几百万年的进化，到各个具体不同的物种
不变的东西，恰恰是在变化中积累下来的，没有变化就分不出什么是变化的，什么是不变的。。
但问题是，什么东西是真正不变的，我们不知道，也不能妄下定论
所以真正永恒的东西，我们还是要把它看成未知数
但是，变化的东西在一个时间段，是有其固定的形式的，他下一个时间段的形式，要靠这个时间段的形式来形成，所以提取不变的东西，是一个迭代的过程

某一经典的形式，必然包含很多的哲学，有很多自描述的，全息性的东西，但表现形式却是十分的简洁，例如，弦乐乐器看似简单，发出的声音却十分复杂；erlang也是这样
从各个方面，各个角度去理解这个形式，都发现很有启发意义，这是经典的东西


2.
函数依赖于数据，执行的先决条件是所需的数据都全了
编译期生成检查数据是否全了的回调方法
全了就执行依赖他的函数
返回期间编译生成 检测是否合乎 数据的定义规范 的回调函数
