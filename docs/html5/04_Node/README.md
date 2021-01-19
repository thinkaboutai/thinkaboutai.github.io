# NodeJS

## 1. Part1 - 基础入门

学习视频：[https://www.bilibili.com/video/BV18K4y1W7wW](https://www.bilibili.com/video/BV18K4y1W7wW)

在学习该知识之前你应该至少掌握`Javascript`

### 1.1 简介

> What is it?

简称 Node，是一个开源的跨平台的 Javascript 运行环境，主要用来创建后端（back-end）服务，即 API（Application Programming Interface）

![](01.png)

> Why use it?

- 开发速度快，适应于敏捷开发（迭代速度快、循序渐进）
- 高扩展性
- 使用`Javascript`编写
- 强大的生态和众多的开源库

> How it works?

在 Node 出现之前：

![](03.png)

- 微软 Edge 的 Chakra
- 谷歌 Chrome 的 v8
- 火狐 Firefox 的 SpiderMonkey

![](02.png)

2009 年，`Ryan Dahl`基于运行速度最快的`Chrome V8`，使用`C++`创建了 Node：

![](04.png)

不再具备`window`、`document`，增加了`os`、`fs`、`http`等新特性。

!> Node 不是一门编程语言（Programming Language），也不是框架（Framework），而是用来执行 Javascript 的运行环境（Runtime Environment）。

> Where？

Node 最大的特性：无阻塞（Non-blocking）/ 异步（Asynchronous）

![](05.png)

相较之 Asp.net，Rails 等框架，要实现异步，需要很多额外的编码工作，而 Node 默认即是以异步模式工作的。

![](06.png)

- 适用于 I/O-intensive 型应用，例如大量读写磁盘、网络连接的应用场景
- 不适用于 CPU-intensive 型应用，例如视频渲染、图片操作的应用场景

### 1.2 安装

NodeJS 中文官网：[https://nodejs.org/zh-cn/](https://nodejs.org/zh-cn/)

下载 LTS（Long-Term Support）版本，别做小白鼠。

可以使用以下指令来检查 Node 版本：

```shell
node --version
```

可以使用以下指令基于旧版本进行更新：

```shell
npm i -g n
n stable
```

### 1.3 Helloworld

### 1.4 Module

### 1.5 NPM

## 2. Part2 - RESTful

## 3. Part3 - MongoDB

## 4. Part4 - Other Topics
