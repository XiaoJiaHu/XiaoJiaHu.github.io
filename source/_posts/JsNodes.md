---
title: JsNodes
date: 2020-08-15 13:35:31
tags:
---
# Command
//将其变为对象
JSON.parse(str)

//指代函数本体 使得函数不用函数名 严格模式不能用
arguments.callee 

//属性 每个函数都有length属性 表示形参长度
fn.length 

//为函数对象
new Function

//删除对象属性 对方法没用 不能删除变量 不能删除原型链的属性
delete

//将add方法的this换做sub 不写默认为代码所在对象
add.call(sub,",")	

//继承的三种方式
原型继承 构造继承 apply call

