# ES6 常用语法梳理

学习视频：[https://www.bilibili.com/video/BV1Mf4y1C7xV](https://www.bilibili.com/video/BV1Mf4y1C7xV)

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

在 ES6 中,数组增加了一些新的方法,其中 map 方法尤其用的之多,结合 ReactJS 的用来动态渲染网页内容非常之好用:

```javascript
const langs = ["Javascript", "golang", "python"];

const items = langs.map((lang) => `<li>${lang}</li>`);
console.log(items);
```

## 6. Object Destructuring

对象析构,又称为对象解构,可以根据名称对应的规则,把一项或者多项属性,从一个对象中解析出来.

```javascript
const product = {
	id: 1,
	name: "Huawei V10",
	category: "phone",
};

// const name = product.name;
// const price = 3000;

const { name, category: type } = product;
```

## 7. Spread Operator

展开操作符,最常用来对数组进行合并、克隆操作

```javascript
const arr1 = [1, 2, 3];
const arr2 = [3, 4, 5];

// const arr = arr1.concat(arr2);
const arr = [...arr1, "x", ...arr2];

const copy = [...arr1];
```

以上写法同样适用于对象

```javascript
const stu = {
	id: 1,
	name: "Jack",
};
const props = {
	gender: "male",
	age: 18,
};

const student = { ...stu, weight: 65, ...props };
const copy = { ...stu };
```

## 8. Class

使用 `JSON` 定义对象的最大短板,就在于对象的方法无法重用,需要书写多次.使用新的类语法来定义可以很好的解决这个问题.

```javascript
class Person {
	constructor(id, name, gender = "male") {
		this.id = id;
		this.name = name;
		this.gender = gender;
	}

	walk() {
		console.log("walk");
	}
}

const p1 = new Person(1, "Jack");
const p2 = new Person(2, "Rose", "female");

console.log(p1, p2);
```

当方法的逻辑需要进行调整的时候,只需要在一处进行修改就可以了.

与其它 OOP 语言一样,JS 的类语法还可以使用继承进行代码的复用:

```javascript
class Student extends Person {
	constructor(id, name, score, gender = "male") {
		super(id, name, gender);
		this.score = score;
	}

	study() {
		console.log("study");
	}
}

const s1 = new Student(1, "Jack", 90);
console.log(s1);
```

!> 子类提供构造器的时候,需要使用 super 调用父类构造器

## 9. Module

在 ES6 中,模块主要使用文件的方式来分割代码

```javascript
export class Person {
	constructor(id, name, gender = "male") {
		this.id = id;
		this.name = name;
		this.gender = gender;
	}

	walk() {
		console.log("walk");
	}
}
```



Module 中所有内容均为私有,要提供给外部使用的话,需使用 `export` 导出.

```javascript
import { Person, other } from "./person";

const p1 = new Person(1, "Jack");
const p2 = new Person(2, "Rose", "female");
console.log(p1, p2);
```



导出分为命名导出( named export )和默认导出( default export )

```javascript
//命名导出
export class Person {}

import { Person } from "./person";

//默认导出
export default class Person {}

import Person from "./person";

//都有
export default class Person{}
export function other(){}

import Person, { other } from "./person"
```

