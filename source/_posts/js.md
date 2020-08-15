---
title: js
date: 2020-08-15 13:35:31
tags:
---
JSON.parse(str)  //将其变为对象

in 判断对象中是否有某个属性 ‘name’ in cat

for (var p in cat)  遍历对象

参数 arguments

arguments.callee 指代函数本体 使得函数不用函数名 严格模式不能用

可以使用 如 var factory = function fn(){};

fn.length 属性 每个函数都有length属性 表示形参长度

if () throw new Error('请传入'，add.ength_'个参数')

var obj = new Function(var1,var2,...,functionBody());

new Function 为函数对象

delete 删除对象属性 对方法没用 不能删除变量 不能删除原型链的属性

add.call(sub,",")	将add方法的this换做sub 不写默认为代码所在对象



继承的三种方式

原型继承 构造继承 apply call

function person(name,age){}

function student(name,age,grade){

this.newMethod = person;	//毛从红person对象 传递特权属性方法（非prototype）给子类

this,newMethod(name,age)

}
