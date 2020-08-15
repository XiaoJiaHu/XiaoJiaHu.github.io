---
title: Vue
date: 2020-08-15 12:44:26
tags:
---
# Vue Day 1
## Base command
- 记录a最新的值和旧的值
vm.$watch('a',function(newVal,oldVal){	})
- 不允许修改
v-once
- 输出真真的html标签
v-html
- 动态绑定一个属性
v-bind : class="mesa" \v-band : class="{ active:isActive }"         缩写 ：
- 指令
v-if=""
- @方法
@click = "click1"       这里点击事件时触发
methods : {click1 : function(){};}
- 是否显示 
v-show
- 迭代对象
v-for = "item in items"
- 绑定点击事件
v-on:click
- 双向绑定
v-model
- 触发事件
this.$emit('',)

## Component
- Vue 声明
var vm= new Vue()
el \ data \ mehthods \ component
- 组件基础
Vue.component(componentName,"")
props \ data \ methods \ template  
- 项目开始
npm run serve
npm run build