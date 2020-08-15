---
title: VueNodes
date: 2020-08-15 12:44:26
tags:
---
# 安装
## 全局安装 vue-cli
npm install --g  @vue/cli
## 安装webpack
npm install -g webpack          
## 创建项目
- 图形化创建一个项目
vue ui    //package管理 设置为npm
- 创建一个基于webpack模板的新项目
vue init webpack my-project     //出错则先运行    npm install -g @vue/cli-init 
 - rooter yes 其他的都 no

## 安装依赖包
cd my-project
npm install     //安装依赖包
npm run serve   //ui让项目跑起来
npm run dev     //webpack让项目跑起来

# files
## src
### config / rem
适配手机屏幕大小
- main.js / import './config/rem'
 - config / rem.js
  ``` (function(){function a(){var b=document.documentElement.clientWidth;b=b>750?750:b;var c=b/750*100;document.getElementsByTagName("html")[0].style.fontSize=c+"px"}a();window.onresize=a})();```

### page / home detail
插入路径
- router / index.js / import Home from '@/page/home'
 - home  ` <template><div class="home-page" >home</div></template> `
 - detail ` <template><div class="detail-page" >detail</div></template><style scoped >.detail-page{width: 20px;}</style>`

## bulid
### px 转 rem
- cnpm install px2rem-loader
- utils.js 
-  ```  var px2remLoader = { 
      loader: 'px2rem-loader',
      options: {
          remUnit:50
      }
  }
  function generateLoaders (loader, loaderOptions) {
    const loaders = options.usePostCSS ? [cssLoader, postcssLoader] : [cssLoader,px2remLoader]      修改此处
- /*no*/ 后面加则不转换 

# Command
## main.js
- Vue 声明
var vm= new Vue()
el \ data \ mehthods \ component
- 组件基础
Vue.component(componentName,"")
props \ data \ methods \ template 


## Base command
vm.$watch('a',function(newVal,oldVal){})        //记录a最新的值和旧的值
v-once      //不允许修改
v-html      // 输出真真的html标签
v-bind : class="mesa" \v-band : class="{ active:isActive }"     //动态绑定一个属性  缩写 ：
v-if=""     //指令
@click = "click1"   methods : {click1 : function(){};}   // @方法 这里点击事件时触发 
v-show      // 是否显示 
v-for = "item in items"     // 迭代对象
v-on:click      // 绑定点击事件
v-model     // 双向绑定
this.$emit('',)     // 触发事件


## template
<router-link to="/detail"></router-link>    //跳转链接
` a{text-decoration: none;} ` 去掉下划线

