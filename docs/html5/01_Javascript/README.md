# Javascript Part1 -- 基础语法
学习视频链：[https://space.bilibili.com/1799937394](https://space.bilibili.com/1799937394)

## 1. 简介

> Javascript是什么？

全世界最常见、最受欢迎的开发语言，其增长的速度一直位居前列。

Stackoverflow 2020调查报告：[https://insights.stackoverflow.com/survey/2020#technology](https://insights.stackoverflow.com/survey/2020#technology)

![](01.png)

良好的市场环境，意味着较高的薪资水平：

职友网2020 前端岗位薪酬：[https://www.jobui.com/salary/quanguo-qianduankaifagongchengshi/](https://www.jobui.com/salary/quanguo-qianduankaifagongchengshi/)

![](02.png)

> Javascript 能做什么？

在早期，主要用来开发基于浏览器的交互应用，但现在已能开发完整的基于PC端、移动端的完整应用，以及实时网络应用（聊天、视频流服务、游戏等）

> Javascript运行在什么地方？

- 浏览器的Javascript引擎，例如Chrome的v8，Firefox的SpiderMonkey
- Node（2009，Ryan基于开源的v8引擎开发的C++程序，可以用作后端服务）

> Javascript由哪些部分组成？

- ECMAScript，描述了该语言的语法和基本对象。
- 文档对象模型（DOM），描述处理网页内容的方法和接口。
- 浏览器对象模型（BOM），描述与浏览器进行交互的方法和接口。

## 2. 环境搭建

Visual Studio Code：[https://code.visualstudio.com/](https://code.visualstudio.com/)

其它的IDE：Sublime Text / Atom / Webstorm

安装Live server扩展（插件）：一个非常轻量级的网站服务器，可以让我们开发的时候，即时看到网站运行效果。

## 3. Helloworld

> 编写和组织Javascript有哪些形式？

- 行内格式
- 分离单独的文件

## 4. 变量和常量

### 4.1 变量

使用变量可以临时的将数据保存在内存中，我们将数据保存在一处，并给它的内存地址一个名字，将来就可以用这个名字来访问这个数据了。

变量命名规则：

- 不能是保留字
- 变量名须有一定意义
- 可以使用英文字符以及“_”和“$”开头
- 不能包含其它特殊字符，如空格和“-”
- 变量名是大小写敏感的

```javascript
let name = 'John';
let age;
age = 20;
let firstName, lastName;
let score = 90, birthday = '2021-1-1';
```

> 最佳实践：使用骆驼命名法来定义变量，一行只定义一个变量。

### 4.2 常量

常量，即是不能修改的“变量”，如果你不需要重新赋值，常量就是最佳选择。

```javascript
const slogan = 'Think About AI';
```

## 5. 数据类型

### 5.1 原始数据类型

Primitive Types / Value Types，也称为值类型：

string / number / boolean / undefined / null / symbol / bigInt

### 5.2 动态语言

Javascript区别于其它很多语言的特点，就在于它是一门动态语言（Dynamic Language）。

> 静态语言：当一个变量被声明后，它的类型就不能修改了。可称为强类型语言。
>
> 动态语言：变量的类型可以在运行时改变，又称为弱类型语言。

```javascript
let flag = 'hello';
console.log(flag); // string
flag = 10;
console.log(flag); //number
```

### 5.3 引用类型

#### 5.3.1 对象

在 Javascript 里，对象可以被看作是一组属性的集合。

```javascript
let stu = {
  id : 1,
  name : 'Jack Ma'
};

console.log(stu);
```

获取对象属性的两种方式：

```javascript
stu.name = 'Mary'; // 对象.属性名
stu['name'] = 'Josh'; // 对象[属性名]
```

> 最佳实践：最常用的是直接使用`.`操作符来访问属性，但如果我们不知道要访问哪个属性时（它本身是个变量，看实际具体情况而定），我们可以使用中括号语法来进行访问。

#### 5.3.2 数组

数组，是用来存储和操作一组（多个）元素的容器。

```javascript
let stus = ['张三','李四','王五'];
```

数组可以通过索引（下标）来进行访问：

```javascript
console.log(stus[0]);
```

> Tips：数组索引从0开始计数

Javascript语言的动态性，在数组上，还可以体现为数组中的元素可以是各种类型，并且，可以动态扩容（改变数组的长度）。而在某些语言中，这是不允许的。

```javascript
stus[2] = 1;
console.log(stus.length); // 3
console.log(typeof stus); // object
```

#### 5.3.3 函数

function，是一组语句，用来执行某些任务，或者进行一些运算。

```javascript
function greet(){
  console.log('Hi');
}

greet();
```

函数可以通过参数来接受输入：

```javascript
function greet(name){
  console.log('Hi ' + name);
}

greet('John');
```

也可以返回运算的结果给调用方：

```javascript
function add(n1, n2){
  return n1 + n2;
}

let res = add(3, 7);
console.log(res);
```

## 6. 操作符

## 7. 流程控制

## 8. 对象

## 9. 数组

## 10. 函数



## 2. Part2 OOP

