---
title: VueNodes
date: 2020-08-15 12:44:26
tags:
---
## start
// 全局安装 vue-cli
npm install --g  @vue/cli

// 安装webpack
npm install -g webpack 

// 创建项目
- 图形化创建一个项目
vue ui    //package管理 设置为npm
- 创建一个基于webpack模板的新项目
vue init webpack my-project     //出错则先运行    npm install -g @vue/cli-init 
 - rooter yes 其他的都 no

// 安装依赖包
cd my-project
npm install     //安装依赖包
npm run serve   //ui让项目跑起来
npm run dev     //webpack让项目跑起来 = npm start 在package.json的scripts里修改

## file config
//适配手机屏幕大小
main.js / import './config/rem'
src / config / rem
(function(){function a(){var b=document.documentElement.clientWidth;b=b>750?750:b;var c=b/750*100;document.getElementsByTagName("html")[0].style.fontSize=c+"px"}a();window.onresize=a})();

//插入路径
router / index.js / import Home from '@/page/home'
home  ` <template><div class="home-page" >home</div></template> `
detail ` <template><div class="detail-page" >detail</div></template><style scoped >.detail-page{width: 20px;}</style>`

//px 转 rem
cnpm install px2rem-loader
build / utils.js 
var px2remLoader = { 
      loader: 'px2rem-loader',
      options: {
          remUnit:50
      }
  }
  function generateLoaders (loader, loaderOptions) {
    const loaders = options.usePostCSS ? [cssLoader, postcssLoader] : [cssLoader,px2remLoader]      修改此处
//不转换rem
/*no*/ 后面加则不转换 

//依赖包
.package.json

//Es6支持转化等
.babelrc

## Command

// Vue 声明
main.js
var vm= new Vue()
el \ data \ mehthods \ component

//组件基础
Vue.component(componentName,"")
props \ data \ methods \ template 

//Base command
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

//跳转链接
<router-link to="/detail"></router-link>    

//去掉下划线
a{text-decoration: none;}

//编译时scss转css app组件不需要配置
<style lang="scss"></style>

//缩写路径
webpack.base.conf.js 见
alias 缩写 extensions 代表后缀可不写
修改了webpack的目录需要重启

//vue-1 
//启动开发是否自动打开浏览器
config / index.js
aotoOpenBrowerser:true
host:'0.0.0.0'

//代码风格 rules下的代码
  - // allow async-await
    'generator-star-spacing': 'off',
    // allow debugger during development
    'no-debugger': process.env.NODE_ENV === 'production' ? 'error' : 'off',
    'semi': ['error', 'always'],
    'indent': 'off',
    'vue/script-indent': ['error', 2, {'baseIndent': 1}],
    'space-before-function-paren': ['error', {'anonymous': 'always', 'named': 'never', 'asyncArrow': 'always'}]
// 自动修改代码
npm run lint -- --fix

//配置src资源
创建src下的目录 pages components base scss js img fonts
移植fonts
_icons.scss 移到scss 
_reset _variables _mixins _base index.scss
- @charest"UTF-8";
  @import"reset";

//删除assets / logo.png
加入资源

//components 删除helloworld

//promise兼容es5 和300ms延迟 --save 导入package --save-dev 开发时依赖
cnpm install --save babel-polyfill fastclick 

//安装scss   开发时的    语法环境  webpack开发依赖
cnpm install --save-dev node-sass sass-loader

//引入scss错误
npm uninstall sass-loader // 卸载当前版本
cnpm install sass-loader@7.3.1 --save-dev 

//安装swiper错误
cnpm install vue-awesome-swiper@3.1.3 -S