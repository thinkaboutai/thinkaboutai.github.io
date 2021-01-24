# ES6 常用语法梳理

学习视频：

## 1. 简介

在学习该视频之前,你应该至少系统的学习过一遍`Javascript`的基础知识,并准备开始进一步学习`NodeJS`、`ReactJS`、`VueJS`等现代流行前端框架.

在这个专题中,不会对ES6的各项语法做深入探讨,如果需要系统学习,请参考:

MDN Javascript 指南:[https://developer.mozilla.org/zh-CN/docs/Web/JavaScript](https://developer.mozilla.org/zh-CN/docs/Web/JavaScript)

环境:`VSCode` + `Live server`

## 2. let vs var

使用 `var` 语法定义变量,最大的特点是其作用域只能通过函数体( function scope )来限定.而没有块级作用域( block scope )的概念.

```javascript
function testScope() {
	for (var i = 0; i < 3; i++) {
		console.log(i);
	}
	console.log("-------");
	console.log(i);
}
```

在 ES6 中,使用 `let` 来定义具有块级作用域的变量( 更符合现代高级语言普遍特性 ),使用 `const` 来定义常量(不能重新赋值):

```javascript
let name = 'Jack';
name = 'Mary';
const slogan = 'Think about AI';
slogan = 'Python'; // error
```

## 3. Object

Javascript中的对象,实际上就是键值对( key - value )的组合.

```javascript
const person = {
  name: 'Jack',
  com: 'com',
  run: function(){}
};
```

如果 key 的 value 一样的话,可以简写成:

```javascript
const person = {
  name: 'Jack',
  com,
  run(){}
};
```

## 4. Arrow function

在 `ES6` 之前:

```javascript
const increment = function (num) {
	return num + 1;
};
```

使用箭头函数:

```javascript
const increment = num => num + 1;
```

> Arrow function & this

当在函数中使用 `this` 的时候,如果用到 `callback` 时,`this` 会绑定到 `window`对象

```javascript
const person = {
	name: "Jack",
	say() {
		setTimeout(function () {
			console.log(this);
		}, 1000);
	},
};
```

由于箭头函数最大的特点在于,它不会重新绑定 `this` ,所以上述可以优化为以下写法:

```javascript
const person = {
	name: "Jack",
	say() {
		setTimeout(() => {
			console.log(this);
		}, 1000);
	},
};
```

## 5. Array.map

## 6. Object Destructuring

## 7. Spread Operator

## 8. Class

## 9. Module