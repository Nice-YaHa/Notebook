# Java简介

## JVM虚拟机（Java虚拟机）

事先在不同操作系统上安装对应版本的JVM，Java程序需要放到JVM中执行，使得不同的操作系统上运行程序得到的结果是一样的，屏蔽底层操作系统的差异性

## Java语言的三大架构

### j2se

给桌面服务提供的解决方案

### j2ee

给企业集中式研发开发提供解决方案

### j2me

给嵌入式开发提供了可能

### jdk1.5

是Java的里程碑式的版本，JAVASE JAVAEE JAVAME

## 搭建Java语言环境

- JRE（Java运行时环境）
  - JRE=JVM + 核心类库（程序启动时必须加载的内容）
- JDK（Java开发工具包，提供运行环境和开发环境）
  - JDK = JRE + kit（开发工具包）

- 配置Java环境

## 入门案例

main方法功能

1. 类不能单独执行，main方法可以让类单独执行
1. main方法是Java所有程序的入口
1. main方法是被jvm调用的



.java文件（程序员可以看懂的内容 源文件）--javac--编译--.class文件（Java可以识别的内容 字节码文件）

.class文件--Java--运行--得到结果





注意：

1. 类的名称和编译生成的.class文件名称一致
1. 公共类的名称要和当前的.Java文件名称一致，如果不是公共类没有要求（公共类只能出现一次）
1. 如果.java文件中有多个类就被编译成多个.class文件
1. 如果.java 文件中有多个类且区分大小写，编译只生成一个.class文件（名称和第一个类的名称一致），内容和最后一个类的内容一样

## Java基本语法组成

1. 关键字

   具有特殊功能的单词，一共具有53个关键字都是小写

2. 标识符

   1. 可以自定义的名称
   2. 组成范围
      1. 常见各国文字
      2. 数字
      3. 特殊符号 _ 、$（慎用）
   3. 命名规则
      1. 不能出现关键字
      2. 不能以数字开头

   在组成范围内只能遵守命名规则的标识符都是合法（符合Java语法）的标识符

3. 命名规范（驼峰命名法）

   1. 类名/接口名	XxxxYyyZzz

   2. 方法名      xxxYyy

   3. 包名（包是用来区分同名类的）   

      1. 单级：xxx
      2. 多级：xxx.xxx.xxx

   4. 常量名：XXX_YYY_ZZZ

      做到见名知意

# Java基本语法组成

## 注释

在代码中用于解释的文字

1. 单行注释

   //注释内容

2. 多行注释

   /*

   注释内容

   */

   可以嵌套单行注释但是不能嵌套多行注释

3. 文档注释

   /**

   注释内容

   */

   可以通过javadoc命令把注释内容生成一个程序员说明书（文档）

4. 

## 常量

在程序运行过程中值不发生改变的量

### 分类

1. 字面值常量
   1. 整数常量 1000 100
   2. 小数常量  2.56
   3. 字符常量 'a'  '6'
   4. 字符串常量 "fdashfklj"
   5. 布尔常量  true false
   6. 空常量  null

2. 自定义常量（面向对象讲）



#### 整数的表现形式

所有的数据都是由计算机底层的硬件的状态来表示的

根据底层的硬件的状态来表示数据，但是可以表示数据的量很小，为了表示更多的数据，把硬件增加到8个

虽然可以表示的数据增多了，但是每次都要查看硬件的状态，为了更高效的表示数据，用0和1去代替硬件的状态

底层出现由0和1来组成的数据（二进制数据）



二进制

​	由0和1组成的数据 以0b开头 0b1010

八进制

​	由0~7组成的数据 以0开头 0754

十进制

​	由0~9组成的数据 默认2345

十六进制

​	由0~9 a~f（不区分大小写） 以0x开头

#### 有符号的数

计算机上所有的数据都是以底层二进制数据的补码形式来表示和操作

原码

​	有符号位。1代表负数，0代表正数

反码：

​	正数的原码和反码一致，负数的反码是在原码的基础上，符号位不变数值位按位取反得到的

补码：

​	整数的原码、反码、补码皆一致，负数是在反码的基础上末尾加1	

#### 小数

​	绝大部分小数转成二进制是无限数

## 变量

在程序执行过程中值可以发生改变的量

`可以存储单个数据的容器`

### 数据类型

限制数据的变化范围

Java是一门强类型编程语言——强制要求`每个数据`都要有数据类型修饰

#### 基本数据类型

整型

​	byte			1			-128~127(-2^7-2^7-1)

​	short			2			-32768~32767(-2^15~2^15-1)

​	int 			4

​	long			8

浮点型

​	float			4

​	double			8

布尔型

​	boolean		1

字符型

​	char			2



char c = '种';

文字转换成底层数字——`编码`  转换过程————码表

ASCII表（阿斯克码表 0~127 底层占用一个字节）————ISO8859-1（西欧码表0~255 底层用一个字节）————Big5（中文繁体 占用俩个字节）、GB2312(中文简体 占用俩个字节)——GBK（国标码 常见中文 占用俩个字节）——Unicode（编码体系 UTF-8 占用三个字节    UTF-16）

`所有的完整码表默认兼容西欧码表`

char c = 'a';  使用U8进行存储，占用1个字节

char c1 = '中';使用U8进行存储，占用3个字节

#### 引用数据类型

数组、类、接口

### 变量名

区分变量名

### 初始化值

为了避免变量操作之前没有赋值

1. `初始化值如果是整数那么默认数据类型是int型`
2. 整数后加上L或者是l就把数据类型表示成long类型
3. `初始化值如果是小数那么默认数据类型是double型`
4. 小数后加上F或者是f就把数据类型表示成float类型
5. `变量在哪定义就在哪使用`

### 定义格式

数据类型 变量名 = 初始化值;

## 操作变量

### 类型转换

1. 类型提升（从小到大 默认）

   byte--short      char--int--long--float--duble 

   整形类型提升为浮点型可能会损失精度

   `byte、short、char类型无论做任何操作都是将类型提升为int类型进行操作`

   

   byte c = 1;

   int a = 1;

   System.out.println(a+c)	



​	short s = 132;

​	char c = s;

​	`short 类型可能会有负数，char没有负数`

​	long --> float 有可能会损失精度



2. 强制类型转换

   目标类型 数据 = （目标类型）数据;

## 运算符

### 算数运算符

+、-、*、/、%、++、--

#### +

1. 求和

当字符型数据遇到数值型会先把字符型数据转化为对应的编码值再进行求和

2. 拼接

字符串常量可以和任意类型的数据进行拼接，字符串常量前面还是正常运算后面都是直接进行拼接

#### /

如果参与运算的都是整数那么结果一定是整数

如果参与运算的有小数，结果一定是小数

不支持整数/0

支持小数/0

#### %

结果的正负由%左边的正负来决定

1%2

-1%2

1%-2

#### ++、--

```java
		int a = 1;
        //a++的值为1
        //把a++当做新变量先接受a的赋值
        System.out.println(a++);
        System.out.println(a);

        a = 1;
        System.out.println(++a);
        System.out.println(a);

```

`总结：`

​	++如果出现在操作数后面先赋值再自加1，如果++出现在操作数的前面先自加1再赋值

​	--如果出现在操作数后面先赋值再自减1，如果--出现在操作数的前面先自减1再赋值

### 赋值运算符

=：右边的值赋给左边

`Java不支持连等定义`

int a = b = c = 1;



连等赋值

```java
int a = 2;
int b = a+=a-=a+=a+5;
System.out.println(a);
System.out.println(b);
```





`底层都添加了强制类型转换`

+=、-=、*=、/=、%=、|=（按位或等）、&=（按位与等）、^=(按位异或等)、>>=(右移等)、<<=（左移等）、>>>=

### 比较（关系）运算符

==、！=、<、>、>=、<=

比较运算符的结果一定是布尔值

### 逻辑运算符

左右俩边都是布尔值

&（逻辑与）|（逻辑或）^（逻辑异或）！（逻辑非）&&（双与）||（双或）

`总结`

&：遇见false就是false

|：遇见true就是true

^:；相同则false，不同则true

！：取反（如果出现的个数是奇数个就取反，偶数个就是本身）

&&：和&的运算规律一致，但是如果&&左边出现false，那么&&右边默认不执行——短路与

||：和|运算规律一致，但是如果||左边出现true，那么||右边默认不执行——短路或

### 位运算符

需要把数据转成底层的`二进制的补码`形式来操作

&（按位与）、|（按位或）、^（按位异或）、~（按位取反）、>>右移、<<左移、>>>无符号右移



按位&：遇0得0

```
00000000 00000000 00000000 00000001 int 1 补码
00000000 00000000 00000000 00000010 int 2 补码
----------------------------------------------
00000000 00000000 00000000 00000000
```

按位|：遇1得1

```
00000000 00000000 00000000 00000001 int 1 补码
00000000 00000000 00000000 00000010 int 2 补码
----------------------------------------------
00000000 00000000 00000000 00000011
```

按位异或^：相同则0，不同则1

​	拓展：

​		和一个整数按位异或俩次结果是本身

```
00000000 00000000 00000000 00000001 int 1 补码
00000000 00000000 00000000 00000010 int 2 补码
----------------------------------------------
00000000 00000000 00000000 00000011
```

​	>>右移：如果是正数往右移动几位就在最高位上补几个0，如果是负数往右移动几位就在最高位上补几个1

`a/(2^移动位数)`

​	<<左移：无论正负数往左移动几位就在最低位上补几个0

`a*(2^移动位数)`

​	>>>无符号右移：无论正负往右移动几位就在最高位补上几个0

`结果一定是整数`



如果是`int类型的数据`，指定的移动位数`需要对32取余`得到的结果才是底层真正移动的位数

如果是`long类型的数据`，指定的移动位数`需要对64取余`得到的结果才是底层真正移动的位数

### 三目（元）运算符

格式

​	布尔表达式 ？表达式值1：表达式值2;

​	如果布尔表达式计算的结果是true返回表达值1

​	如果布尔表达式计算的结果是false返回表达值2

​	`俩个表达式值的类型可以不一样但是要保证在接受类型范围`

## 

## 

## 流程控制语句

### 选择结构

#### if结构

#### switch语句

格式:

​	Switch（表达式1）{

​		case 值1：

​			语句;

​			break;

​		case 值2：

​			语句;

​			break;

​		case 值3：

​			语句;

​			break;

​		...

​		default:

​			语句;

​			break;

​	}

`注意`

1. 表达式的值支持的类型byte、short、char、int，从jdk1.5后支持枚举类型，jdk1.7后支持String类型
2. case的值是一个常量，不能重复
3. break可以省略，会出现case穿透效果(输入月份返回季节适用)
4. default可以省略不写
5. 语句结束的标志：
   1. 遇见break
   2. 没有break语句执行到最后一行结束


### 循环结构

for、while、dowhile

#### for

​	解决循环范围已知的问题

#### while

​	解决循环范围不确定的问题

#### dowhile

格式

​	初始值

​	do{

​		循环体;

​		控制条件;

​	}while（判断条件）;

执行流程

> 计算出初始值，执行循环体，执行控制条件改变初始值，拿着改变的初始值和判断条件进行比较。如果比较的结果是true执行循环体执行控制条件改变初始值，再拿着改变的初始值和判断条件进行比较，如果是true就重复上述操作直到比较结果是false循环结束

#### 三种循环体

1. 三种循环`等效转换`
2. for适合循环范围确定，while循环适合循环范围确定，dowhile最少执行一次
3. 三种循环都有可能出现死循环

### 跳转控制语句

#### break

结束当前循环

#### continue

跳过当次循环

#### return(方法)

## 数组

可以存储`多个相同数据类型`元素的`容器`

### 定义格式

1. 数据类型[] 数组名 = new 数据类型[数组的长度/元素的个数]

```java
		int[] num = new int[3];
        System.out.println(num);
```

[I@a57993

> [:代表是数组类型
>
> I：代表是int类型
>
> @：表示后面是地址值
>
> a57993：十六进制的哈希码值

通过数组名（数组地址）可以找到数组，数组底层根据数组元素会自动进行编号（从0开始），由数组地址值和编号共同可以唯一确定数组中元素---`数组名[下标]`

2. 数据类型[] 数组名 = new 数据类型[]{元素1，元素2，元素3......};
3. 数据类型[] 数组名 ={元素1，元素2，元素3......};

new---在堆内存开辟新空间

系统默认给定初始值（byte\short\int\long---0、char---'\u0000'--u16码表、float---0.0F、Boolean---false、引用数据类型---null）

### Java内存分区

栈

堆

方法区（面向对象讲）

本地方法栈（不讲）

寄存器（不讲）

#### 栈

存储的是变量，如果存储内容不再使用立即清除,不会堆存储内容赋予系统默认初始值

#### 堆

存储的是对象，如果存储的对象不再使用会在某个时刻由操作系统来进行回收，会对存储的内容赋予系统默认初始值

![2022-01-01_180228](D:\Note\pictures\2022-01-01_180228.png)

### 数组的应用

#### 遍历

依次输出数组元素值

#### 最值

数组最大值最小值 

#### 查找

给定查找数，根据查找返回在数组第一次出现的下标

- 二分查找，基于`二分思想`进行的查找
  - 缺点：有序、查找数靠前查找也慢

#### 排序

给数组元素大小进行排列顺序

- 冒泡排序

  ```java
  public class bullbleSort {
      public static void main(String[] args) {
          int temp = 0;
          int[] nums = {9,8,7,6,5,4,3,2,1};
          for (int i = 0; i < nums.length; i++) {
              for (int j = nums.length-1; j > i ; j--) {
                  if (nums[j-1]>nums[j]){
                      temp = nums[j-1];
                      nums[j-1] = nums[j];
                      nums[j] = temp;
                  }
              }
          }
          System.out.println(Arrays.toString(nums));
      }
  }
  ```

  

- 选择排序

  

#### 扩容

数组定义完长度不变，数组的复制

数组的复制

> System.arraycopy(arr,0,new_arr,0,arr.length);

数组的扩容

只能从头开始复制

​					（要复制的数组，新长度）

> arr = Arrays.copyOf(arr,arr.length*2);

### 二维数组

![2022-01-01_220459](D:\Note\pictures\2022-01-01_220459.png)

## 方法

对重复且有效的代码进行抽取，抽取的形式就是方法

java方法不存在嵌套

书写格式

​	修饰符 返回值类型 方法名 （参数类型 参数名...){

​		方法体;

​		return 返回值;

​	}

`注意`

1. 方法必须`调用`才能执行

2. 抽取方法时明确返回值类型和参数列表

3. return的俩个作用

   1. 返回值
   2. 结束方法

4. 如果方法有返回值需要考虑所有的取值情况再给定对应的操作以及对应的返回值

5. Java中所有的方法执行是加载到栈里面执行

6. 如果参数传入的是引用数据类型，则操作会改变其值

   如果是基本数据类型，操作不会改变

### 重载

在一个类中，方法名一致但是参数列表不一致

如果出现精确匹配的方法进行精确匹配，如果没有出现精确匹配方法但是出现相对精确的匹配方法做相对精确匹配。如果出现多个相对精确匹配方法不能调用到指定方法会报错。



# 面向对象简介

> 本质是一种编程范式（套路  思考方式）
>
> > 面向过程
> >
> > ​	关注的是代码的实现细节
>
> >面向对象
> >
> >​	先把代码的实现细节整合到对象身上，关注对象，只要找到了对象就能拥有对象身上的功能
>
> 面向对象基于面向过程，面向对象优于面向过程？不一定，场景越简单优先推荐面向过程，场景越复杂优先推荐面向对象

类和对象的关系

​	对同一类对象进行抽取，把共同的特征信息抽取成属性，把共同的行为信息抽取成方法，把这一类对象抽取成类

## 构造方法

类中没有定义构造方法底层会默认提供一个无参构造，类中定义有参构造底层就不会提供无参构造。（类中至少有一个构造方法来保证类可以被实例化）

有参构造可以对属性进行初始化



构造方法`没有返回值类型`，与类同名



`Java中所有的非静态方法和非静态属性都需要通过对象调用`



### this

关键字，代表当前类的对象

1. 代表当前类的正在创建的对象
2. 代表当前类正在操作的对象
3. 可以代表类还没有创建的对象

### this（）

this语句，在当前方法中，调用别的构造方法`只能在首行`

### super

关键字，代表父类对象

### super()

super语句，在子类构造方法中调用父类构造方法

`子类所有的构造方法默认使用super无参语句调用父类无参构造`

如果父类没有提供无参构造每个子类的构造方法需要手动写super有参调用父类对应的有参构造

父类对象优于子类对象先出现`（父子类执行顺序（对象级别） 父类构造代码块--父类构造方法--子类构造代码块--子类构造方法 ）`

## 构造代码块

类内方法外{}

属性初始化

优先于`所有的构造方法先执行`

## 局部代码块

方法内出现一个{}

控制变量的生命周期，提高内存的利用率

## 成员变量和局部变量

### 位置

成员变量：类内方法外

局部变量：方法内

### 使用范围

成员变量：整个类内

局部变量：方法内

### 内存

成员变量：堆

局部变量：栈

### 生命周期

成员变量：随着类创建对象而出现，随着对象的销毁而销毁

局部变量：随着方法的调用而出现，随着方法调用结束而消失

# 面向对象的特征

封装、继承、多态（抽象）

## 封装

方便以后代码的维护

体现形式---方法  属性私有化，提供公共访问方式在外部可以正常的操作私有化属性值，提高数据的安全性

## 继承

多个类中出现相同的内容放到一个新的类中，通过extends让原来的类和新的类产生继承关系。原来的类称之为子类，新的类称之为父类。子类继承父类部分信息----私有的继承不到、构造方法、构造代码块

### 继承方式（单继承）

一个类只能有一个父类，一个父类可以有多个子类

### 重写（覆盖）

在父子类中出现方法签名一致的方法

`原则`

两等两小一大

1. 方法签名一致（重写的前提）

2. 如果父类方法的返回值类型是基本数据类型/void，那么子类方法返回值类型和父类的方法的返回值类型保持一致

3. 如果父类方法的返回值是引用数据类型，那么子类的方法返回值类型要么和父类的方法返回值类型保持一致要么是父类方法返回值类型的子类

4. 子类方法访问权限休息符要么和父类方法访问权限修饰符一致，要么要比父类方法的访问权限修饰符要大

### 访问权限修饰符（控制在那些位置关系下可以获取信息）

|           | 本类 | 同包类 |   子类   | 其他类 |
| :-------: | :--: | :----: | :------: | :----: |
|  public   |  √   |   √    |    √     |   √    |
| protected |  √   |   √    |    √     |   ×    |
|   默认    |  √   |   √    | 同包子类 |   ×    |
|  private  |  √   |   ×    |    ×     |   ×    |

## 多态

在程序操作过程中可以展示多种形式

### 编译时期（体现形式--重载）

在编译时期绑定代码

### 运行时期（体现形式--重写、向上造型  前提是继承）

在运行时期绑定代码

#### 向上造型

声明类是父类，实际创建对象的类是子类---向上造型---可以调用哪些方法看父类，调用的方法具体执行看子类是否有重写



优点：

1. 参数统一对象
2. 解耦（降低耦合度）

## static

修饰符  变量、方法、代码块、内部类

### 静态变量（静态的成员变量）

静态变量随着类的加载（方法区的静态常量池）而加载到静态区（`和类一个级别`），会给静态变量赋予系统默认初始值。静态变量也称之为类变量，可以通过类名的形式来调用静态变量也可以通过对象调用静态变量。创建的多个对象共享同一个静态变量。

（如果需要属性被所有对象来共享就可以加上static）



方法中可以定义静态变量吗？

> 不可以
>
> 方法被调用里面的内容才出现，但是静态变量与类同级，所以前后矛盾，不能定义

### 静态方法

静态方法随着类的加载（方法区的静态常量池）而加载到静态区，不会赋予初始值。静态方法与类同级，也叫类方法，既可以通过类名调用，也可以通过对象调用。`静态方法存储在静态区，但是当静态方法被调用就会被加载到栈中执行`



`静态信息（属性和方法）只能直接操作静态信息，非静态信息可以直接操作静态信息以及非静态信息`



静态方法可以定义静态变量？

> 不可以
>
> 方法被调用里面的内容才出现，但是静态变量与类同级，所以前后矛盾，不能定义



静态方法支持重载？

> 支持重载



静态方法支持重写？

> 不支持
>
> 静态方法与类同级没有重写，允许父子类中出现方法签名一致的俩个静态方法（没有重写）或者俩个非静态方法（有重写）

### 静态代码块

在类内方法外{}用static修饰

将静态属性初始化，预先加载一些资源

优先于构造代码块先执行

随着类的加载`只加载一次`（静态信息（变量、方法）代码块等等随着类的加载只加载一次）



## 父子类执行顺序

父类静态信息--子类静态信息--父类对象级别（成员变量，构造代码块，构造方法）--子类对象级别成员变量，构造代码块，构造方法）

## final

关键字  修饰符 值、方法、类



### 最终值

​	final修饰基本类型数据的值不能改变

​	final修饰的引用类型数据的地址值不能改变

​	final修饰的是成员变量必须在对象创建完成之前进行初始化

​	final修饰的是静态变量（静态常量）必须在类加载完成之前进行初始化

### 最终方法

支持重载但是不能重写

### 最终类

可以有父类但是没有子类

## abstract（抽象）

所有的子类都对父类中的某个方法进行了不同程度的重写，那么这个方法的方法体没有任何意义就可以去掉但是需要加上abstract关键字来修饰就变成抽象方法，普通类中出现抽象方法需要把普通类变成abstract类。普通继承抽象类需要重写所有的抽象方法，如果不想重写所有抽象方法需要把普通类变成抽象类即可

`注意`

1. 抽象方法（没有方法体、必须要被重写）

2. 抽象类中可以定义属性和方法？

   可以

3. 抽象类可以定义构造方法？

   可以

4. 抽象类可以创建对象？

   不能，底层是由别的编程语言来构建，Java获取不到这个对象就是没有对象。 

5. 抽象类一定含有抽象方法？

​	不一定

6. 抽象方法可以被static/final/private分别修饰？

​	不能

7. 抽象类可以被final修饰？

   不能

8. 抽象类的目的延展类的继承结构

## interface（接口）

抽象类中所有的方法都是抽象方法，可以通过interface关键字变成接口。接口的本质不是类。普通类和接口通过implement关键字产生实现关系，接口与接口之间支持多继承，类与接口之间支持多实现（为了丰富类的功能）。普通类实现接口需要重写所有的抽象方法如果不需要重写可以把普通类变成抽象类。

`注意`

1. 接口可以定义构造方法？

   不能

2. 接口可以创建对象？

   不能

3. 接口里的方法都是抽象方法？

   是的（暂且）

4. 接口可以定义属性？

   可以，但是`属性`默认被`public static final` 共同修饰，`抽象方法`默认被`public abstract` 共同修饰

5. 声明一个接口对象可以在编译期间接受任意对象的赋值但是要在运行时间检测是否是接口的实现类

6. 接口的目的为了丰富实现类的功能（注入新的特性）

​	

![2022-01-05_155554](D:\Note\pictures\2022-01-05_155554.png)

> 在编译期间检测俩个对象的声明类是否有继承关系
>
> 在运行期间检测俩个对象的实际创建类是否一致

`注`：

类和接口支持多实现形成的是网状图不能快速确定俩者之间的关系，所以编译期间不检测，运行检测是否是接口的实现类



### 接口和抽象类的区别

1. 接口都是抽象方法
2. 接口有构造方法
3. 接口支持多继承、接口和类支持多实现
4. 接口不是类
5. 接口定义属性和抽象方法都有默认的修饰符来修饰
6. 抽象类是为了延展类的继承结构，接口是为了丰富实现类的功能

### 接口的优点

约束、模板

## 内部类

### 类内部定义类

#### 方法内部类

```java
class outer{
    public void m(){
        class inner{
    		
        }
    }  
}
```

1. 可以定义所有的非静态信息（方法和属性）以及静态常量

2. 可以正常的继承和实现

3. 类可以被final和abstract来修饰

4. 方法内部类可以获取外部类所有的信息

5. 只能获取当前方法中的常量信息

6. 只能在本方法中创建内部类对象

#### 成员内部类

```java
public class innerDemo1 {
    public static void main(String[] args) {
        outer.Inner inner =new outer().inner（）;
        outer.Inner inner1 = new outer().new Inner();
        System.out.println(inner.j);
    }
}
class outer{
    int i = 1;

    Inner inner = new Inner();

    class Inner{
        int j =1;
    }

    public void m(){

    }
 }
```

1. 可以定义所有的非静态信息（方法和属性）以及静态常量
2. 可以正常的继承和实现
3. 可以被四个访问权限修饰符来修饰
4. 可以获取外部类所有的信息
5. 创建内部类

#### 静态内部类（static修饰内部类一定是静态内部类）

```java
public class innerDemo1 {
    public static void main(String[] args) {
        outer.Inner inner =new outer.inner（）;
        System.out.println(inner.j);
    }
}
abstract class outer{
    int i = 1;

    Inner inner = new Inner();

    class Inner{
        int j =1;
    }

    public void m(){

    }
 }
```

1. 可以定义所有的非静态信息（方法和属性）以及静态常量
2. 可以正常的继承和实现
3. 可以被四个访问权限修饰符来修饰
4. 可以获取外部类所有的静态信息
5. 创建内部类

#### 匿名内部类

```java
public class innerDemo1 {
    public static void main(String[] args) {
        //{}是匿名内部类
        //默认继承类（除了最终类）重写抽象方法
        //接口依然可以有匿名内部类的形式，默认实现接口重写抽象方法
        inner in = new inner() {
            @Override
            public void m() {
                
            }
        };
    }
   
}
abstract class inner{
    public abstract void m();
}
```

1. 可以默认继承类/实现接口，重写抽象方法
2. 常用于参数传递

### 接口内部定义类以及内部接口都默认被static修饰

```java
public class innerDemo1 {
    public static void main(String[] args) {
        System.out.println(outer.inner.i);
    }
}
interface outer{
    class inner{
        static int i =1;
    }
}
```

## 垃圾回收机制（GC）

### 产生垃圾的内存分区

堆（主要产生垃圾）

### 垃圾回收

堆内存分为新生代和老生代，新生代分为伊甸园区和幸存区。新建的对象存放在新生代的伊甸园区，系统扫描一次如果这个对象没有被使用就会被系统进行回收，如果仍然还在使用就会挪到幸存区。系统堆幸存区扫描多次，如果这个对象没有在使用会被系统进行回收，如果仍然在使用就会把这个对象挪到老生代。系统对老生代扫描多次（频率要比幸存区低）如果这个对象没有在使用就被系统进行回收如果仍在使用还是存放在老生代

![2022-01-06_121118](D:\Note\pictures\2022-01-06_121118.png)

## 包

### 使用包

声明包	指定包名（类或者接口所在的位置）	在首行且最多只能有一个

导入包	和当前类不再一个位置下（包下）的类或者接口来进行导入	不再首行但是在类前可以有多个*代表当前包下的所有类或者所有接口

### 提供包

Java（提供的是Java源生包）

​	lang包：程序启动必须加载的内容（核心类库），使用时无需导包

​	util包：提供操作对象和类的工具包（工具包）

​	io包：提供数据传输

​	math包:提供简单的数学运算

​	net包：网络传输

​	nio包：高并发

​	security：安全

​	sql包：操作数据库

​	time包：操作时间和日期

Javax（提供的是Java的拓展包）

org（第三方厂商）

# API---Application Programing Interfaces

# （应用程序接口--提供一系列接口和类）

## Object类

是所有类的父类，所有的类默认继承Object类

### 主要方法

### clone（）

返回克隆对象

把原对象的属性值赋值到新对象中并且返回新对象

类实现cloneable接口产生的对象才支持克隆，Cloneable接口没有内容只是克隆的标志，当类实现这个接口，类就会拥有一个标志

只能在本类中创建子类对象才能在其他位置访问到protect修饰的信息

### finalize（）

通知系统进行垃圾回收

### getClass() 

返回object的实际创建类的类型（形式为：包名+类名）

### hashCode()

返回对象的哈希码值，`此处为十进制 `

不同对象的哈希码值不一样

#### 哈希码值的特点

1. 取值范围广---数据重复概率小
2. 均匀分布

`由上述俩个特点导致哈希码值没有重复---哈希码值是唯一的`

内存地址值唯一，可以由哈希码值来表示内存地址

### toSting（）

object类中的toString（）方法在拼接对象地址值并且返回

底层会默认让对象调用Object类中的toSting方法才返回对象的地址值

需要重写toSting（）方法展示对象的属性

### equals（）

此方法根据地址值来判定俩个对象是否相等

#### 重写equals（）方法

```java
class Person{
    String name;
    int age;
    char gender;

    //重写equals方法---根据对象地址值和对象属性值综合判断两个对象是否相等
    @Override
    public boolean equals(Object obj) {
        //1.判断对象地址值是否相等
        if(this==obj){//this代表当前类正在活动的对象  调用equals方法的对象
            return true;
        }

        //2.判断参数对象是否为null值
        if(obj==null){
            return false;
        }

        //3.判断对象类型是否一致
        if(this.getClass()!=obj.getClass()){
            return false;
        }


        //从逻辑上代码执行到此可以保证两个对象的类型一致
        //但是从语法上参数obj的类型是Object不能拿到对应的属性只能强转成Person类型
        Person p=(Person) obj;


        //4.判断对象属性值
        //判断对象的age属性值是否相等
        if(this.age!=p.age){
            return false;
        }
        //判断对象的gender属性值是否相等
        if(this.gender!=p.gender){
            return false;
        }
        //判断对象的name属性值是否相等
        //代码执行到此表面age和gender一定相同
        //不仅要比较name对象的地址值还要比较name对象的内容
        //p.name.equals(this.name)  p.name代表String类型的对象  调用String类重写的equals方法
        //重写的内容既比较地址值也比较对象的内容
        if(p.name==this.name||p.name!=null&&p.name.equals(this.name)){
            return true;
        }

        //对象属性name不相同
        return false;
    }
}

```

## String类



























































