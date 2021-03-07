# Java 快速入门

## Part1 - 基础语法

学习视频：

### 1. Java 概述

#### 1.1 Java 语言背景介绍（了解）

语言：人与人交流沟通的表达方式

计算机语言：人与计算机之间进行信息交流沟通的一种特殊语言

Java 语言是美国 Sun 公司（ Stanford University Network ）在 1995 年推出的计算机语言

Java 之父：詹姆斯·高斯林（ James Gosling ）

2009 年， Sun 公司被甲骨文公司收购，所以我们现在访问 Oracle 官网即可：[https://www.oracle.com](https://www.oracle.com/)

Java 语言的三个版本：

- JavaSE : Java 语言的（标准版），用于桌面应用的开发，是其他两个版本的基础

- JavaME : Java 语言的（小型版），用于嵌入式消费类电子设备

- JavaEE : Java 语言的（企业版），用于 Web 方向的网站开发

#### 1.2 Java 语言跨平台原理（理解）

Java 程序并非是直接运行的，Java 编译器将 Java 源程序编 译成与平台无关的字节码文件( class 文件 )，然后由 Java 虚拟机（ JVM ）对字节码文件解释执行。所以在不同的操作系统下，只需安装不同的 Java 虚拟机即可实现 Java 程序的跨平台。

#### 1.3 JRE 和 JDK（记忆）

JVM（ Java Virtual Machine ），Java 虚拟机

JRE（ Java Runtime Environment ），Java 运行环境，包含了 JVM 和 Java 的核心类库（ Java API ）

JDK（ Java Development Kit ）称为 Java 开发工具，包含了 JRE 和开发工具

总结：我们只需安装 JDK 即可，它包含了 Java 的运行环境和虚拟机。

#### 1.4 JDK 的下载和安装（应用）

##### 1.4.1 下载

通过官方网站获取 JDK

[http://www.oracle.com](http://www.oracle.com/)

> 注意：针对不同的操作系统，需要下载对应版本的 JDK。

##### 1.4.2 安装

傻瓜式安装，下一步即可。但默认的安装路径是在 C:\Program Files 下，为方便统一管理建议修改安装路径，将与开发相关的软件都安装到一个目录下，例如：E:\develop。

**注意**：安装路径不要包含中文或者空格等特殊字符（使用纯英文目录）。

##### 1.4.3 JDK 的安装目录介绍

| 目录名称 | 说明                                                              |
| -------- | ----------------------------------------------------------------- |
| bin      | 该路径下存放了 JDK 的各种工具命令。javac 和 java 就放在这个目录。 |
| conf     | 该路径下存放了 JDK 的相关配置文件。                               |
| include  | 该路径下存放了一些平台特定的头文件。                              |
| jmods    | 该路径下存放了 JDK 的各种模块。                                   |
| legal    | 该路径下存放了 JDK 各模块的授权文档。                             |
| lib      | 该路径下存放了 JDK 工具的一些补充 JAR 包。                        |

### 2. 第一个演示程序

#### 2.1 常用 DOS 命令（应用）

在接触集成开发环境之前，我们需要使用命令行窗口对 java 程序进行编译和运行，所以需要知道一些常用 DOS 命令。

1、打开命令行窗口的方式：`win + r` 打开运行窗口，输入 `cmd` ，回车。

2、常用命令及其作用

| 操作                 | 说明                                |
| -------------------- | ----------------------------------- |
| 盘符名称:            | 盘符切换。E:回车，表示切换到 E 盘。 |
| dir                  | 查看当前路径下的内容。              |
| cd 目录              | 进入单级目录。cd hnguigu            |
| cd ..                | 回退到上一级目录。                  |
| cd 目录 1\目录 2\... | 进入多级目录。cd hnguigu\JavaSE     |
| cd \                 | 回退到盘符目录。                    |
| cls                  | 清屏。                              |
| exit                 | 退出命令提示符窗口。                |

#### 2.2 Path 环境变量的配置（应用）

> 为什么配置环境变量

开发 Java 程序，需要使用 JDK 提供的开发工具（ 比如 javac.exe 、java.exe 等命令），而这些工具在 JDK 的安装目录的 bin 目录下，如果不配置环境变量，那么这些命令只可以在该目录下执行。我们不可能把所有的 java 文件都放到 JDK 的 bin 目录下，所以配置环境变量的作用就是可以使 bin 目录下的 java 相关命令可以在任意目录下使用。

#### 2.3 HelloWorld案例（应用）

HelloWorld案例是指在计算机屏幕上输出“HelloWorld”这行文字。

使用VS Code演示该案例。

##### 2.3.1 Java程序开发运行流程

开发Java程序，需要三个步骤：编写程序，编译程序，运行程序。

##### 2.3.2 HelloWorld案例的编写

1、新建文本文档文件，修改名称为HelloWorld.java。

2、用记事本打开HelloWorld.java文件，输写程序内容。

~~~java
public class HelloWorld {
	public static void main(String[] args) {
		System.out.println("HelloWorld");
	}
}
~~~

##### 2.3.3 HelloWorld案例的编译和运行

存文件，打开命令行窗口，将目录切换至java文件所在目录，编译java文件生成class文件，运行class文件。

> 编译：javac 文件名.java
>
> 范例：javac HelloWorld.java
>
> 执行：java 类名
>
> 范例：java HelloWorld

#### 2.4 HelloWorld案例详解（理解）



#### 2.5 Helloworld案例常见问题(理解)

##### 2.5.1 BUG

##### 2.5.2 BUG的解决

##### 2.5.3 Helloworld案例常见问题

#### 2.6 IDEA软件的安装和使用（应用）

##### 2.6.1 什么要使用IDEA软件

IDEA王者荣耀

##### 2.6.2 IDEA软件安装

安装：傻瓜式安装，一直下一步即可。建议也安装到统一的开发软件目录下，比如E:\develop。

##### 2.6.3 IDEA软件配置

安装完毕之后，为了使用方便，做一个简单的配置：修改默认语言和编码。

### 3. Java基础语法

#### 3.1 标识符（理解）

- 标识符是用户编程时使用的名字，用于给类、方法、变量、常量等命名。


- Java中标识符的组成规则：
  - 由字母、数字、下划线“_”、美元符号“$”组成，第一个字符不能是数字。
  - 不能使用java中的关键字作为标识符。	
  - 标识符对大小写敏感（区分大小写）。

- Java中标识符的命名约定：（重要）
  - 小驼峰式命名：变量名、方法名
    - 首字母小写，从第二个单词开始每个单词的首字母大写。
  - 大驼峰式命名：类名
    - 每个单词的首字母都大写。
  - 另外，标识符的命名最好可以做到**见名知意**
    - 例如：username、studentNumber等。
  - 常量必须全大写，如果有多个单词组词需要使用“_”来分割
  - 包名称必须全小写

#### 3.2 注释（理解）

注释是对代码的解释和说明文字，可以提高程序的可读性，因此在程序中添加必要的注释文字十分重要。Java中的注释分为三种：

单行注释。单行注释的格式是使用//，从//开始至本行结尾的文字将作为注释文字。

~~~java
// 这是单行注释文字
~~~

多行注释。多行注释的格式是使用/* 和 */将一段较长的注释括起来。

~~~java
/*
这是多行注释文字
这是多行注释文字
这是多行注释文字
*/
注意：多行注释不能嵌套使用。
~~~

文档注释。文档注释以`/**`开始，以`*/`结束。（以后讲）

#### 3.3 关键字（理解）

关键字是指被java语言赋予了特殊含义的单词。

关键字的特点：

​	关键字的字母全部小写。

​	常用的代码编辑器对关键字都有高亮显示，比如现在我们能看到的public、class、static等。

#### 3.4 常量（应用）

常量：在程序运行过程中，其值不可以发生改变的量。

Java中的常量分类：

​	字符串常量  用双引号括起来的多个字符（可以包含0个、一个或多个），例如"a"、"abc"、"中国"等

​	整数常量  整数，例如：-10、0、88等

​	小数常量  小数，例如：-5.5、1.0、88.88等

​	字符常量  用单引号括起来的一个字符，例如：'a'、'5'、'B'、'中'等

​	布尔常量  布尔值，表示真假，只有两个值true和false

​	空常量  一个特殊的值，空值，值为null

除空常量外，其他常量均可使用输出语句直接输出。

~~~java
public class Demo {
    public static void main(String[] args) {
        System.out.println(10); // 输出一个整数
        System.out.println(5.5); // 输出一个小数
        System.out.println('a'); // 输出一个字符
        System.out.println(true); // 输出boolean值true
        System.out.println("欢迎来到湖南硅谷"); // 输出字符串
    }
}
~~~

#### 3.5 变量的介绍(理解)

变量的定义格式：

​	数据类型 变量名 = 数据值；

​	数据类型：为空间中存储的数据加入类型限制。整数？小数？

​	变量名：自己要为空间起的名字，没有难度

​	数据值： 空间中要存储的数值，没有难度

#### 3.6 变量（应用）

##### 3.6.1 变量的定义

变量：在程序运行过程中，其值可以发生改变的量。

从本质上讲，变量是内存中的一小块区域，其值可以在一定范围内变化。

变量的定义格式：

```java
数据类型 变量名 = 初始化值; // 声明变量并赋值
int age = 18;
System.out.println(age);
```

或者(扩展)

```java
// 先声明，后赋值（使用前赋值即可）
数据类型 变量名;
变量名 = 初始化值;
double money;
money = 55.5;
System.out.println(money);
```

还可以(扩展)

在同一行定义多个同一种数据类型的变量，中间使用逗号隔开。但不建议使用这种方式，降低程序的可读性。

```java
int a = 10, b = 20; // 定义int类型的变量a和b，中间使用逗号隔开
System.out.println(a);
System.out.println(b);

int c,d; // 声明int类型的变量c和d，中间使用逗号隔开
c = 30;
d = 40;
System.out.println(c);
System.out.println(d);
```

##### 3.6.2 变量的修改

```java
int a = 10;
a = 30;  //修改变量的值
System.out.println(a);
```

变量前面不加数据类型时，表示修改已存在的变量的值。

##### 3.6.3 变量的注意事项(理解)

1. 在同一对花括号中，变量名不能重复。
2. 变量在使用之前，必须初始化（赋值）。
3. 定义long类型的变量时，需要在整数的后面加L（大小写均可，建议大写）。因为整数默认是int类型，整数太大可能超出int范围。
4. 定义float类型的变量时，需要在小数的后面加F（大小写均可，建议大写）。因为浮点数的默认类型是double， double的取值范围是大于float的，类型不兼容。

#### 3.7 数据类型（应用）

##### 3.7.1 Java中的数据类型

Java是一个强类型语言，Java中的数据必须明确数据类型。在Java中的数据类型包括**基本数据类型**和**引用数据类型**两种。

Java中的基本数据类型：4类8种

| 数据类型 |    关键字    | 内存占用 | 取值范围                                                     |
| :------: | :----------: | :------: | :----------------------------------------------------------- |
| 整数类型 |     byte     |    1     | -128~127                                                     |
|          |    short     |    2     | -32768~32767                                                 |
|          |  int(默认)   |    4     | -2的31次方到2的31次方-1                                      |
|          |     long     |    8     | -2的63次方到2的63次方-1                                      |
| 浮点类型 |    float     |    4     | 负数：-3.402823E+38到-1.401298E-45<br />正数：   1.401298E-45到3.402823E+38 |
|          | double(默认) |    8     | 负数：-1.797693E+308到-4.9000000E-324<br />正数：4.9000000E-324   到1.797693E+308 |
| 字符类型 |     char     |    2     | 0-65535                                                      |
| 布尔类型 |   boolean    |    1     | true，false                                                  |

说明：

​	e+38表示是乘以10的38次方，同样，e-45表示乘以10的负45次方。

​	在java中整数默认是int类型，浮点数默认是double类型。

#### 3.8 键盘录入（理解）

我们可以通过 Scanner 类来获取用户的输入。使用步骤如下：

1、导包。Scanner 类在java.util包下，所以需要将该类导入。导包的语句需要定义在类的上面。

```java
import java.util.Scanner; 
```

2、创建Scanner对象。

```java
Scanner sc = new Scanner(System.in);// 创建Scanner对象，sc表示变量名，其他均不可变
```

3、接收数据

```java
int i = sc.nextInt(); // 表示将键盘录入的值作为int数返回。
```

示例：

```java
import java.util.Scanner;
public class ScannerDemo {
	public static void main(String[] args) {
		//创建对象
		Scanner sc = new Scanner(System.in);
		//接收数据
		int a = sc.nextInt();
		//输出数据
		System.out.println(a);
	}
}
```

#### 3.9 算术运算符

##### 3.9.1 运算符和表达式（了解）

运算符：对常量或者变量进行操作的符号

表达式：用运算符把常量或者变量连接起来符合java语法的式子就可以称为表达式。

​                    不同运算符连接的表达式体现的是不同类型的表达式。

举例说明：

```java
int a = 10;
int b = 20;
int c = a + b;
```

  +：是运算符，并且是算术运算符。

  a + b：是表达式，由于+是算术运算符，所以这个表达式叫算术表达式。

#####  3.9.2 算术运算符(应用)

| 符号 | 作用 | 说明                         |
| ---- | ---- | ---------------------------- |
| +    | 加   | 参看小学一年级               |
| -    | 减   | 参看小学一年级               |
| *    | 乘   | 参看小学二年级，与“×”相同    |
| /    | 除   | 参看小学二年级，与“÷”相同    |
| %    | 取余 | 获取的是两个数据做除法的余数 |

注意：

1. /和%的区别：两个数据做除法，/取结果的商，%取结果的余数。

2. 整数操作只能得到整数，要想得到小数，必须有浮点数参与运算。

~~~java
int a = 10;
int b = 3;
System.out.println(a / b); // 输出结果3
System.out.println(a % b); // 输出结果1
~~~

##### 3.9.3 字符的“+”操作（理解）

char类型参与算术运算，使用的是计算机底层对应的十进制数值。需要我们记住三个字符对应的数值：

'a'  --  97		a-z是连续的，所以'b'对应的数值是98，'c'是99，依次递加

'A'  --  65		A-Z是连续的，所以'B'对应的数值是66，'C'是67，依次递加

'0'  --  48		0-9是连续的，所以'1'对应的数值是49，'2'是50，依次递加

~~~java
// 可以通过使用字符与整数做算术运算，得出字符对应的数值是多少
char ch1 = 'a';
System.out.println(ch1 + 1); // 输出98，97 + 1 = 98

char ch2 = 'A';
System.out.println(ch2 + 1); // 输出66，65 + 1 = 66

char ch3 = '0';
System.out.println(ch3 + 1); // 输出49，48 + 1 = 49
~~~

算术表达式中包含不同的基本数据类型的值的时候，整个算术表达式的类型会自动进行提升。

提升规则：

**byte类型，short类型和char类型将被提升到int类型，不管是否有其他类型参与运算。**

**整个表达式的类型自动提升到与表达式中最高等级的操作数相同的类型**

​       等级顺序：byte,short,char --> int --> long --> float --> double

例如：

~~~java
byte b1 = 10;
byte b2 = 20;
// byte b3 = b1 + b2; // 该行报错，因为byte类型参与算术运算会自动提示为int，int赋值给byte可能损失精度
int i3 = b1 + b2; // 应该使用int接收
byte b3 = (byte) (b1 + b2); // 或者将结果强制转换为byte类型
-------------------------------
int num1 = 10;
double num2 = 20.0;
double num3 = num1 + num2; // 使用double接收，因为num1会自动提升为double类型
~~~

##### 3.9.4 字符串的“+”操作（理解）

当“+”操作中出现字符串时，这个”+”是字符串连接符，而不是算术运算。

~~~java
System.out.println("hnguigu"+ 666); // 输出：hnguigu666
~~~

在”+”操作中，如果出现了字符串，就是连接运算符，否则就是算术运算。当连续进行“+”操作时，从左到右逐个执行。

~~~java
System.out.println(1 + 99 + "年湖南硅谷");            // 输出：100年湖南硅谷
System.out.println(1 + 2 + "hnguigu" + 3 + 4);   // 输出：3hnguigu34
// 可以使用小括号改变运算的优先级 
System.out.println(1 + 2 + "hnguigu" + (3 + 4)); // 输出：3hnguigu7
~~~

##### 3.9.5 数值拆分（应用）

需求：

​	键盘录入一个三位数，将其拆分为个位，十位，百位，打印在控制台

示例代码：

```java
import java.util.Scanner;
public class Test {
	public static void main(String[] args) {
		// 1：使用Scanner键盘录入一个三位数
		Scanner sc = new Scanner(System.in);
		System.out.println("请输入一个三位数");
		int num = sc.nextInt();
		// 2：个位的计算：数值 % 10
		int ge = num % 10;		
		// 3：十位的计算：数值 / 10 % 10
		int shi = num / 10 % 10;	
		// 4：百位的计算：数值 / 100
		int bai = num / 100;
		// 5：将个位, 十位, 百位拼接上正确的字符串, 打印即可
		System.out.println("整数"+num+"个位为:" + ge);
		System.out.println("整数"+num+"十位为:" + shi);
		System.out.println("整数"+num+"百位为:" + bai);
		
	}
}
```

#### 3.10 自增自减运算符（理解）

| 符号 | 作用 | 说明        |
| ---- | ---- | ----------- |
| ++   | 自增 | 变量的值加1 |
| --   | 自减 | 变量的值减1 |

注意事项：

​	++和-- 既可以放在变量的后边，也可以放在变量的前边。

​	单独使用的时候， ++和-- 无论是放在变量的前边还是后边，结果是一样的。

​	参与操作的时候，如果放在变量的后边，先拿变量参与操作，后拿变量做++或者--。

​	参与操作的时候，如果放在变量的前边，先拿变量做++或者--，后拿变量参与操作。

​	最常见的用法：单独使用。

```java
int i = 10;
i++; // 单独使用
System.out.println("i:" + i); // i:11

int j = 10;
++j; // 单独使用
System.out.println("j:" + j); // j:11

int x = 10;
int y = x++; // 赋值运算，++在后边，所以是使用x原来的值赋值给y，x本身自增1
System.out.println("x:" + x + ", y:" + y); // x:11，y:10

int m = 10;
int n = ++m; // 赋值运算，++在前边，所以是使用m自增后的值赋值给n，m本身自增1
System.out.println("m:" + m + ", m:" + m); // m:11，m:11
```

练习：

```java
int x = 10;
int y = x++ + x++ + x++;
System.out.println(y); // y的值是多少？
```

#### 3.11 赋值运算符（应用）

赋值运算符的作用是将一个表达式的值赋给左边，左边必须是可修改的，不能是常量。

| 符号 | 作用       | 说明                  |
| ---- | ---------- | --------------------- |
| =    | 赋值       | a=10，将10赋值给变量a |
| +=   | 加后赋值   | a+=b，将a+b的值给a    |
| -=   | 减后赋值   | a-=b，将a-b的值给a    |
| *=   | 乘后赋值   | a*=b，将a×b的值给a    |
| /=   | 除后赋值   | a/=b，将a÷b的商给a    |
| %=   | 取余后赋值 | a%=b，将a÷b的余数给a  |

注意：

扩展的赋值运算符隐含了强制类型转换。

~~~java
short s = 10;
s = s + 10; // 此行代码报出，因为运算中s提升为int类型，运算结果int赋值给short可能损失精度

s += 10; // 此行代码没有问题，隐含了强制类型转换，相当于 s = (short) (s + 10);
~~~

#### 3.12 关系运算符（应用）

关系运算符有6种关系，分别为小于、小于等于、大于、等于、大于等于、不等于。

| 符号 | 说明                                                    |
| ---- | ------------------------------------------------------- |
| ==   | a==b，判断a和b的值是否相等，成立为true，不成立为false   |
| !=   | a!=b，判断a和b的值是否不相等，成立为true，不成立为false |
| >    | a>b，判断a是否大于b，成立为true，不成立为false          |
| >=   | a>=b，判断a是否大于等于b，成立为true，不成立为false     |
| <    | a<b，判断a是否小于b，成立为true，不成立为false          |
| <=   | a<=b，判断a是否小于等于b，成立为true，不成立为false     |

注意事项：

​	关系运算符的结果都是boolean类型，要么是true，要么是false。

​	千万不要把“==”误写成“=”，"=="是判断是否相等的关系，"="是赋值。

~~~java
int a = 10;
int b = 20;
System.out.println(a == b); // false
System.out.println(a != b); // true
System.out.println(a > b); // false
System.out.println(a >= b); // false
System.out.println(a < b); // true
System.out.println(a <= b); // true

// 关系运算的结果肯定是boolean类型，所以也可以将运算结果赋值给boolean类型的变量
boolean flag = a > b;
System.out.println(flag); // 输出false
~~~

#### 3.13 逻辑运算符（应用）

逻辑运算符把各个运算的关系表达式连接起来组成一个复杂的逻辑表达式，以判断程序中的表达式是否成立，判断的结果是 true 或 false。

| 符号 | 作用     | 说明                                         |
| ---- | -------- | -------------------------------------------- |
| &    | 逻辑与   | a&b，a和b都是true，结果为true，否则为false   |
| \|   | 逻辑或   | a\|b，a和b都是false，结果为false，否则为true |
| ^    | 逻辑异或 | a^b，a和b结果不同为true，相同为false         |
| !    | 逻辑非   | !a，结果和a的结果正好相反                    |

~~~java
//定义变量
int i = 10;
int j = 20;
int k = 30;

//& “与”，并且的关系，只要表达式中有一个值为false，结果即为false
System.out.println((i > j) & (i > k)); //false & false,输出false
System.out.println((i < j) & (i > k)); //true & false,输出false
System.out.println((i > j) & (i < k)); //false & true,输出false
System.out.println((i < j) & (i < k)); //true & true,输出true
System.out.println("--------");

//| “或”，或者的关系，只要表达式中有一个值为true，结果即为true
System.out.println((i > j) | (i > k)); //false | false,输出false
System.out.println((i < j) | (i > k)); //true | false,输出true
System.out.println((i > j) | (i < k)); //false | true,输出true
System.out.println((i < j) | (i < k)); //true | true,输出true
System.out.println("--------");

//^ “异或”，相同为false，不同为true
System.out.println((i > j) ^ (i > k)); //false ^ false,输出false
System.out.println((i < j) ^ (i > k)); //true ^ false,输出true
System.out.println((i > j) ^ (i < k)); //false ^ true,输出true
System.out.println((i < j) ^ (i < k)); //true ^ true,输出false
System.out.println("--------");

//! “非”，取反
System.out.println((i > j)); //false
System.out.println(!(i > j)); //!false，,输出true
~~~

#### 3.14 短路逻辑运算符（理解）

| 符号 | 作用   | 说明                         |
| ---- | ------ | ---------------------------- |
| &&   | 短路与 | 作用和&相同，但是有短路效果  |
| \|\| | 短路或 | 作用和\|相同，但是有短路效果 |

在逻辑与运算中，只要有一个表达式的值为false，那么结果就可以判定为false了，没有必要将所有表达式的值都计算出来，短路与操作就有这样的效果，可以提高效率。同理在逻辑或运算中，一旦发现值为true，右边的表达式将不再参与运算。

- 逻辑与&，无论左边真假，右边都要执行。

- **短路与&&，如果左边为真，右边执行；如果左边为假，右边不执行。**

- 逻辑或|，无论左边真假，右边都要执行。

- **短路或||，如果左边为假，右边执行；如果左边为真，右边不执行。**

~~~java
int x = 3;
int y = 4;
System.out.println((x++ > 4) & (y++ > 5)); // 两个表达都会运算
System.out.println(x); // 4
System.out.println(y); // 5

System.out.println((x++ > 4) && (y++ > 5)); // 左边已经可以确定结果为false，右边不参与运算
System.out.println(x); // 4
System.out.println(y); // 4
~~~

#### 3.15 三元运算符（理解）

三元运算符语法格式：

~~~java
关系表达式 ? 表达式1 : 表达式2;
~~~

解释：问号前面的位置是判断的条件，判断结果为boolean型，为true时调用表达式1，为false时调用表达式2。其逻辑为：如果条件表达式成立或者满足则执行表达式1，否则执行第二个。

举例：

~~~java
int a = 10;
int b = 20;
int c = a > b ? a : b; // 判断 a>b 是否为真，如果为真取a的值，如果为假，取b的值
~~~

#### 3.16 三元运算符案例(应用)

需求：有三个学生，已知他们的身高分别为150cm、210cm、165cm，请用程序实现获取这三个学生的最高身高。

~~~java
public class OperatorTest02 {
	public static void main(String[] args) {
		//1：定义三个变量用于保存学生的身高，单位为cm，这里仅仅体现数值即可。
		int height1 = 150;
		int height2 = 210;
		int height3 = 165;	
		//2：用三元运算符获取前两个学生的较高身高值，并用临时身高变量保存起来。
		int tempHeight = height1 > height2 ? height1 : height2;		
		//3：用三元运算符获取临时身高值和第三个学生身高较高值，并用最大身高变量保存。
		int maxHeight = tempHeight > height3 ? tempHeight : height3;	
		//4：输出结果
		System.out.println("maxHeight:" + maxHeight);
	}
}
~~~

### 4. 流程控制语句

在一个程序执行的过程中，各条语句的执行顺序对程序的结果是有直接影响的。所以，我们必须清楚每条语句的执行流程。而且，很多时候要通过控制语句的执行顺序来实现我们想要的功能。

#### 4.1 流程控制语句分类(了解)

​	顺序结构

​	分支结构(if, switch)

​	循环结构(for, while, do…while)

#### 4.2 顺序结构(了解)

顺序结构是程序中最简单最基本的流程控制，没有特定的语法结构，按照代码的先后顺序，依次执行，程序中大多数的代码都是这样执行的。

顺序结构执行流程图：

![1545615769372](图片2.png)

#### 4.3 分支结构之if语句

##### 4.3.1 if语句格式1（理解）

~~~java
格式：
if (关系表达式) {
    语句体;	
}
~~~

执行流程：

①首先计算关系表达式的值

②如果关系表达式的值为true就执行语句体

③如果关系表达式的值为false就不执行语句体

④继续执行后面的语句内容

![1545616039363](图片3.png)

示例：

~~~java
public class IfDemo {
	public static void main(String[] args) {
		System.out.println("开始");
        
		// 如果年龄大于18岁, 就可以上网吧
		int age = 17;
		
		if(age >= 18){
			// int a = 10;
			System.out.println("可以上网吧");
		}
			
		System.out.println("结束");
	}
}
~~~

##### 4.3.2 if语句格式2（理解）

~~~java
格式：
if (关系表达式) {
    语句体1;	
} else {
    语句体2;	
}
~~~

执行流程：

①首先计算关系表达式的值

②如果关系表达式的值为true就执行语句体1

③如果关系表达式的值为false就执行语句体2

④继续执行后面的语句内容

![1545616221283](图片4.png)

示例：奇偶数

​	任意给出一个整数，请用程序实现判断该整数是奇数还是偶数，并在控制台输出该整数是奇数还是偶数。

~~~java
public class Demo2If {
	public static void main(String[] args) {
		// 程序判断一个数, 是奇数还是偶数
		int num = 9;
		
		if(num % 2 == 0){
			System.out.println("偶数");
		}else{
			System.out.println("奇数");
		}
	}
}
~~~

##### 4.3.3 if语句格式3（理解）

~~~java
格式：
if (关系表达式1) {
    语句体1;	
} else if (关系表达式2) {
    语句体2;	
} 
…
else {
    语句体n+1;
}
~~~

执行流程：

①首先计算关系表达式1的值

②如果值为true就执行语句体1；如果值为false就计算关系表达式2的值

③如果值为true就执行语句体2；如果值为false就计算关系表达式3的值

④…

⑤如果没有任何关系表达式为true，就执行语句体n+1。

![1545616667104](图片5.png)

示例：

​	定义一个在0~100之间的变量a, 90~100优秀，80~89良好，70~79中等，60~69及格，0~59请努力加油！

~~~java
public class Demo3If {
	public static void main(String[] args){
		int score = 65;
		if(score >= 90 && score <= 100){
			System.out.println("优秀");
		}else if (score >= 80 && score <= 89){
			System.out.println("良好");
		}else if (score >= 70 && score <= 79){
			System.out.println("中等");
		}else if (score >= 60 && score <= 69){
			System.out.println("及格");
		}else if (score >= 0 && score <= 59){
			System.out.println("请努力加油");
		}else{
			System.out.println("成绩有误!");
		}
	}
}
~~~

#### 4.4 switch语句

##### 4.4.1 分支语句switch语句

* 格式

  ```java
  switch (表达式) {
  	case 1:
  		语句体1;
  		break;
  	case 2:
  		语句体2;
  		break;
  	...
  	default:
  		语句体n+1;
  		break;
  }
  ```

* 执行流程：

  * 首先计算出表达式的值 
  * 其次，和case依次比较，一旦有对应的值，就会执行相应的语句，在执行的过程中，遇到break就会结 束。 
  * 最后，如果所有的case都和表达式的值不匹配，就会执行default语句体部分，然后程序结束掉。 

##### 4.4.2 switch案例-减肥计划

* 需求：键盘录入星期数，显示今天的减肥活动

```
周一：跑步  
周二：游泳  
周三：慢走  
周四：动感单车
周五：拳击  
周六：爬山  
周日：好好吃一顿 
```

* 示例代码：

```java
public static void main(String[] args){
		// 1. 键盘录入星期数据，使用变量接收
		Scanner sc = new Scanner(System.in);
		System.out.println("请输入");
		int week = sc.nextInt();
		// 2. 多情况判断，采用switch语句实现
		switch(week){
			// 3. 在不同的case中，输出对应的减肥计划
			case 1:
				System.out.println("跑步");
				break;
			case 2:
				System.out.println("游泳");
				break;
			case 3:
				System.out.println("慢走");
				break;
			case 4:
				System.out.println("动感单车");
				break;
			case 5:
				System.out.println("拳击");
				break;
			case 6:
				System.out.println("爬山");
				break;
			case 7:
				System.out.println("好好吃一顿");
				break;
			default:
				System.out.println("您的输入有误");
				break;
		}
	}
}
```

##### 4.4.3 switch语句case穿透

- 概述 : 如果switch语句中,case省略了break语句, 就会开始case穿透
- 需求 : 键盘录入星期数，输出工作日、休息日 (1-5)工作日，(6-7)休息日
- 示例代码：

```java
/*
case穿透是如何产生的?
		
		如果switch语句中,case省略了break语句, 就会开始case穿透.
		
		现象：
			当开始case穿透，后续的case就不会具有匹配效果，内部的语句都会执行
			直到看见break，或者将整体switch语句执行完毕，才会结束。
*/
public static void main(String[] args){
		Scanner sc = new Scanner(System.in);
		System.out.println("请输入星期数:");
		int week = sc.nextInt();
		
		switch(week){
			case 1:
			case 2:
			case 3:
			case 4:
			case 5:
				System.out.println("工作日");
				break;
			case 6:
			case 7:
				System.out.println("休息日");
				break;
			default:
				System.out.println("您的输入有误");
				break;
		}
	}	
}
```

#### 4.5. for循环

##### 4.5.1 循环语句-for循环

* 循环：

  循环语句可以在满足循环条件的情况下，反复执行某一段代码，这段被重复执行的代码被称为循环体语句，当反复 执行这个循环体时，需要在合适的时候把循环判断条件修改为false，从而结束循环，否则循环将一直执行下去，形 成死循环。 

* for循环格式：

```java
for (初始化语句;条件判断语句;条件控制语句) {
	循环体语句;
}
```

* 格式解释：

  * 初始化语句：  用于表示循环开启时的起始状态，简单说就是循环开始的时候什么样
  * 条件判断语句：用于表示循环反复执行的条件，简单说就是判断循环是否能一直执行下去
  * 循环体语句：  用于表示循环反复执行的内容，简单说就是循环反复执行的事情
  * 条件控制语句：用于表示循环执行中每次变化的内容，简单说就是控制循环是否能执行下去

* 执行流程：

  ①执行初始化语句

  ②执行条件判断语句，看其结果是true还是false

  ​             如果是false，循环结束

  ​             如果是true，继续执行

  ③执行循环体语句

  ④执行条件控制语句

  ⑤回到②继续

##### 4.5.2 for循环案例-输出数据1-5和5-1

* 需求：在控制台输出1-5和5-1的数据 
* 示例代码：

```java
public class ForTest01 {
    public static void main(String[] args) {
		//需求：输出数据1-5
        for(int i=1; i<=5; i++) {
			System.out.println(i);
		}
		System.out.println("--------");
		//需求：输出数据5-1
		for(int i=5; i>=1; i--) {
			System.out.println(i);
		}
    }
}
```

##### 4.5.3 for循环案例-求1-5数据和

* 需求：求1-5之间的数据和，并把求和结果在控制台输出 
* 示例代码：

```java
public class ForTest02 {
    public static void main(String[] args) {
		//求和的最终结果必须保存起来，需要定义一个变量，用于保存求和的结果，初始值为0
		int sum = 0;
		//从1开始到5结束的数据，使用循环结构完成
		for(int i=1; i<=5; i++) {
			//将反复进行的事情写入循环结构内部
             // 此处反复进行的事情是将数据 i 加到用于保存最终求和的变量 sum 中
			sum += i;
			/*
				sum += i;	sum = sum + i;
				第一次：sum = sum + i = 0 + 1 = 1;
				第二次：sum = sum + i = 1 + 2 = 3;
				第三次：sum = sum + i = 3 + 3 = 6;
				第四次：sum = sum + i = 6 + 4 = 10;
				第五次：sum = sum + i = 10 + 5 = 15;
			*/
		}
		//当循环执行完毕时，将最终数据打印出来
		System.out.println("1-5之间的数据和是：" + sum);
    }
}
```

* 本题要点：
  * 今后遇到的需求中，如果带有求和二字，请立即联想到求和变量
  * 求和变量的定义位置，必须在循环外部，如果在循环内部则计算出的数据将是错误的

##### 4.5.4 for循环案例-求1-100偶数和

* 需求：求1-100之间的偶数和，并把求和结果在控制台输出 }
* 示例代码：

```java
public class ForTest03 {
    public static void main(String[] args) {
		//求和的最终结果必须保存起来，需要定义一个变量，用于保存求和的结果，初始值为0
		int sum = 0;
		//对1-100的数据求和与1-5的数据求和几乎完全一样，仅仅是结束条件不同
		for(int i=1; i<=100; i++) {
			//对1-100的偶数求和，需要对求和操作添加限制条件，判断是否是偶数
			if(i%2 == 0) {
				sum += i;
			}
		}
		//当循环执行完毕时，将最终数据打印出来
		System.out.println("1-100之间的偶数和是：" + sum);
    }
}
```

##### 4.5.5 for循环案例-水仙花数

* 需求：在控制台输出所有的“水仙花数” 
* 解释：什么是水仙花数？
  * 水仙花数，指的是一个三位数，个位、十位、百位的数字立方和等于原数
    * 例如`153  3*3*3 + 5*5*5 + 1*1*1 = 153`
* 思路：
  1. 获取所有的三位数，准备进行筛选，最小的三位数为100，最大的三位数为999，使用for循环获取
  2. 获取每一个三位数的个位，十位，百位，做if语句判断是否是水仙花数
* 示例代码

```java
public class ForTest04 {
    public static void main(String[] args) {
		//输出所有的水仙花数必然要使用到循环，遍历所有的三位数，三位数从100开始，到999结束
		for(int i=100; i<1000; i++) {
			//在计算之前获取三位数中每个位上的值
			int ge = i%10;
			int shi = i/10%10;
			int bai = i/10/10%10;
			
			//判定条件是将三位数中的每个数值取出来，计算立方和后与原始数字比较是否相等
			if(ge*ge*ge + shi*shi*shi + bai*bai*bai == i) {
				//输出满足条件的数字就是水仙花数
				System.out.println(i);
			}
		}
    }
}
```

#### 4.6 while循环

##### 4.6.1 循环语句-while循环

* while循环完整格式：

  ```java
  初始化语句;
  while (条件判断语句) {
  	循环体语句;
      条件控制语句;
  }
  ```

* while循环执行流程：

  ①执行初始化语句

  ②执行条件判断语句，看其结果是true还是false

  ​             如果是false，循环结束

  ​             如果是true，继续执行

  ③执行循环体语句

  ④执行条件控制语句

  ⑤回到②继续

* 示例代码：

```java
public class WhileDemo {
    public static void main(String[] args) {
        //需求：在控制台输出5次"HelloWorld"
		//for循环实现
		for(int i=1; i<=5; i++) {
			System.out.println("HelloWorld");
		}
		System.out.println("--------");
		//while循环实现
		int j = 1;
		while(j<=5) {
			System.out.println("HelloWorld");
			j++;
		}
    }
}
```

#### 4.7 循环细节

##### 4.7.1 循环语句-dowhile循环

* 完整格式：

  ```java
  初始化语句;
  do {
  	循环体语句;
  	条件控制语句;
  }while(条件判断语句);
  ```

* 执行流程：

  ① 执行初始化语句

  ② 执行循环体语句

  ③ 执行条件控制语句

  ④ 执行条件判断语句，看其结果是true还是false

  如果是false，循环结束

  如果是true，继续执行

  ⑤ 回到②继续

* 示例代码：

```java
public class DoWhileDemo {
    public static void main(String[] args) {
        //需求：在控制台输出5次"HelloWorld"
		//for循环实现
		for(int i=1; i<=5; i++) {
			System.out.println("HelloWorld");
		}
		System.out.println("--------");
		//do...while循环实现
		int j = 1;
		do {
			System.out.println("HelloWorld");
			j++;
		}while(j<=5);
    }
}
```

##### 4.7.2 三种循环的区别

* 三种循环的区别
  * for循环和while循环先判断条件是否成立，然后决定是否执行循环体（先判断后执行）
  * do...while循环先执行一次循环体，然后判断条件是否成立，是否继续执行循环体（先执行后判断）
* for循环和while的区别
  * 条件控制语句所控制的自增变量，因为归属for循环的语法结构中，在for循环结束后，就不能再次被访问到了
  * 条件控制语句所控制的自增变量，对于while循环来说不归属其语法结构中，在while循环结束后，该变量还可以继续使用

##### 4.7.3 跳转控制语句

* 跳转控制语句（break）
  * 跳出循环，结束循环
* 跳转控制语句（continue）
  * 跳过本次循环，继续下次循环
* 注意： continue只能在循环中进行使用！

```java
public class Demo1Continue {
	/*
		continue : 跳过某次循环体内容的执行
		
		注意：使用是基于条件控制, 在循环内部使用.
		
		需求: 模拟电梯上行的过程 1-24层, 4层不停.
	*/
	public static void main(String[] args){
		for(int i = 1; i <= 24; i++){
			if(i == 4){
				continue;
			}
			System.out.println(i + "层到了~");
		}
	}
	
}
```

```java
public class Demo2Break {
	/*
		break : 终止循环体内容的执行
		注意：使用是基于条件控制的
				break语句只能在循环和switch中进行使用.
				
		需求: 模拟20岁工作到80岁, 60岁退休.
	*/
	public static void main(String[] args){
		for(int i = 20; i <= 80; i++){
			if(i == 60){
				break;		// 结束整个循环
			}
			System.out.println(i + "岁正在上班");
		}
	}
	
}
```

```java
import java.util.Scanner;

public class Test {
	/*
		需求：程序运行后，用户可多次查询星期对应的减肥计划，直到输入0，程序结束
		
		步骤:
			
			1. 不明确用户操作几次, 使用死循环包裹业务逻辑
			2. 匹配到0的时候，使用break结束循环死循环

	*/
	public static void main (String[] args){
		
		lo:while(true){
			System.out.println("请输入您要查看的星期数:");
			System.out.println("(如无需继续查看,请输入0退出程序)");
			
			// 1. 键盘录入星期数据，使用变量接收
			Scanner sc = new Scanner(System.in);
			int week = sc.nextInt();
			// 2. 多情况判断，采用switch语句实现
			switch(week){
				// 3. 在不同的case中，输出对应的减肥计划
				case 0:
					System.out.println("感谢您的使用");
					break lo;
				case 1:
					System.out.println("跑步");
					break;
				case 2:
					System.out.println("游泳");
					break;
				case 3:
					System.out.println("慢走");
					break;
				case 4:
					System.out.println("动感单车");
					break;
				case 5:
					System.out.println("拳击");
					break;
				case 6:
					System.out.println("爬山");
					break;
				case 7:
					System.out.println("好好吃一顿");
					break;
				default:
					System.out.println("您的输入有误");
					break;
			}
		}
		
		
	}
}
```

### 5. Random

#### 5.1 Random产生随机数（掌握）

* 概述：

  * Random类似Scanner，也是Java提供好的API，内部提供了产生随机数的功能

* 使用步骤：

  1. 导入包

     import java.util.Random;

  2. 创建对象

     Random r = new Random();

  3. 产生随机数

     int num = r.nextInt(10);

     解释： 10代表的是一个范围，如果括号写10，产生的随机数就是0-9，括号写20，参数的随机数则是0-19

* 示例代码：

```java
import java.util.Random;

public class Demo1Random {
	/*
		Random : 产生随机数
		
		1. 导包	: import java.util.Random;
				    导包的动作必须出现在类定义的上面

		2. 创建对象 : Random r = new Random();
					上面这个格式里面，r 是变量名，可以变，其他的都不允许变

		3. 获取随机数 : int number = r.nextInt(10);	//获取数据的范围：[0,10) 包括0,不包括10
					上面这个格式里面，number是变量名，可以变，数字10可以变。其他的都不允许变
		
		需求: 产生随机数1-10之间的
	*/
	public static void main(String[] args){
		// 2. 创建对象
		Random r = new Random();
		
		for(int i = 1; i <= 10; i++){
			// 3. 获取随机数
			int num = r.nextInt(10) + 1;		// 1-10
			System.out.println(num);
		}
		
		
		
	}
}
```

#### 5.2 Random练习-猜数字（应用）

* 需求：

  程序自动生成一个1-100之间的数字，使用程序实现猜出这个数字是多少？

  当猜错的时候根据不同情况给出相应的提示

  A. 如果猜的数字比真实数字大，提示你猜的数据大了

  B. 如果猜的数字比真实数字小，提示你猜的数据小了

  C. 如果猜的数字与真实数字相等，提示恭喜你猜中了

* 示例代码：

```java
import java.util.Scanner;
import java.util.Random;

public class Test {
	/*
		需求：程序自动生成一个1-100之间的数字，使用程序实现猜出这个数字是多少？
			当猜错的时候根据不同情况给出相应的提示
			如果猜的数字比真实数字大，提示你猜的数据大了
			如果猜的数字比真实数字小，提示你猜的数据小了
			如果猜的数字与真实数字相等，提示恭喜你猜中了
		
		1. 准备Random和Scanner对象, 分别用于产生随机数和键盘录入
		2. 使用Random产生一个1-100之间的数, 作为要猜的数
		3. 键盘录入用户猜的的数据
		4. 使用录入的数据(用户猜的数据)和随机数(要猜的数据)进行比较, 并给出提示
		
		5. 以上内容需要多次进行, 但无法预估用户输入几次可以猜测正确, 使用while(true)死循环包裹
		6. 猜对之后, break结束.

	*/
	public static void main(String[] args){
		// 1. 准备Random和Scanner对象, 分别用于产生随机数和键盘录入
		Random r = new Random();
		Scanner sc = new Scanner(System.in);
		// 2. 使用Random产生一个1-100之间的数, 作为要猜的数
		int randomNum = r.nextInt(100) + 1;
		
		// 5. 以上内容需要多次进行, 但无法预估用户输入几次可以猜测正确, 使用while(true)死循环包裹
		while(true){
			// 3. 键盘录入用户猜的的数据
			System.out.println("请输入您猜的数据:");
			int num = sc.nextInt();
			// 4. 使用录入的数据(用户猜的数据)和随机数(要猜的数据)进行比较, 并给出提示
			if(num > randomNum){
				System.out.println("猜大了");
			}else if(num < randomNum){
				System.out.println("猜小了");
			}else{
				// 6. 猜对之后, break结束.
				System.out.println("恭喜,猜中了");
				break;
			}
		}
		
		System.out.println("感谢您的使用");
		
	}
}
```



## Part2 - OOP

## Part3 - Advanced
