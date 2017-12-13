---
layout: post
title: "JavaScript - 함수의 종류"
date:   2017-12-12 11:04:00
author: C-an
categories: JavaScript
---

#### 1. 선언적 함수 ####
##### -1 #####
```javascript
function show(){
	...
}
```
##### -2 #####
```javascript
var show = function show(){
	...
}
```
#### 2. 익명 함수 ####
```javascript
var show = function (){
	...
}
```

자바스트립트에서는 크게 두 가지, 세부적으로는 세 가지의 경우로 함수를 작성할 수 있다.

**1** 선언적함수 1의 경우에는 언제 어디서든지 해당 함수를 사용할 수 있지만 선언적함수 2와 익명 함수는 함수 선언 이후에서만 사용이 가능하다란 큰 차이점이 있다.

**2** 또한 선언적함수 1과는 달리 선언적함수 2와 익명 함수는 **var show**란 변수에 할당을 하였는데 이때 객체(Object)로 사용이 된다.

이것은 다른 언어와는 달리 함수가 객체로도 사용이 된다는 것인데, 예를 들면 다음과 같다.

```javascript
var show = function show(){
	...
}

show.foo = "Hello, World!";
show.num = 2;

console.log(show.foo);   // Hello, World!
console.log(show.num);   // 2
```
**3** 또한, 익명 함수는 Java에서의 익명 클래스처럼 단 한 번만 사용될 때 사용되는 특징이 있다.

**4** 함수를 변수에 대입을 시키면
```javascript
document.write(foo);

/*
function show(){...}
*/
```
와 같은 결과를 얻는다. (즉, 그냥 함수 리터럴(자체)가 들어있다.)

**5** 함수 내에 var없이 변수를 정의하게 되면 Global Variable이 된다.(**Node.js**에서는 좀 다르다.)