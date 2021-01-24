# ES6 常用语法梳理

学习视频：

## 1. 简介

在学习该视频之前,你应该至少系统的学习过一遍`Javascript`的基础知识,并准备开始进一步学习`NodeJS`、`ReactJS`、`VueJS`等现代流行前端框架.

在这个专题中,不会对ES6的各项语法做深入探讨,如果需要系统学习,请参考:

阮一峰 ECMAScript6 入门教程:[https://es6.ruanyifeng.com/](https://es6.ruanyifeng.com/)

环境:`VSCode` + `Live server`

## 1. let vs var

使用 `var` 语法定义变量,最大的特点是其作用域只能通过函数体(function scope)来限定.而没有块级作用域(block scope)的概念.

```javascript
function testScope() {
	for (var i = 0; i < 3; i++) {
		console.log(i);
	}
	console.log("-------");
	console.log(i);
}
```

在 ES6 中,使用 `let` 来定义具有块级作用域的变量(更符合现代高级语言普遍特性),使用 `const` 来定义常量(不能重新赋值):

```javascript
let name = 'Jack';
name = 'Mary';
const slogan = 'Think about AI';
slogan = 'Python'; // error
```

## 2. Object

Javascript中的对象,实际上就是键值对(key-value)的组合.

```javascript
const person = {
  name: 'Jack',
  com: 'com',
  run: function(){}
};
```

如果key的value一样的话,可以简写成:

```javascript
const person = {
  name: 'Jack',
  com,
  run(){}
};
```

## 3. Arrow function

## 4. Array.map

## 5. Object Destructuring

## 6. Spread Operator

## 7. Class

## 8. Module