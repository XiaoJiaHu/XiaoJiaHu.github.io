---
title: CssNodes
date: 2020-08-15 12:43:52
tags:
---
# Flex
## Flex
- 排布方向
flex-direction: row   \ column   \ row-reverse   \ colume   \ reverse
- 对齐方式
justify-content: center   \ flex-start \ flex-end \ space-around \ space-evenly \ space-between
align-items: center   \ flex-start   \ flex-end
- 是否换行
flex-warp: nowrap   \ warp
- 缩写 flex-direction   \ and   \ flex-warp
flex-flow: row   \ nowrap
- 行与行之间的对其方式
align-content：   \ flex-start   \ center   \ flex-end   \ initial   \ space-around   \ space-evenly   \ space-between

## Flex Item
- 排序位置
order:1
- 覆写alignitems
align-self: center   \ flex-start   \ flex-end 
- 主轴方向大小
flex-basis: 100px   \ 0   \ auto;
- 占主轴剩余空间份数（扩大）
__lex-grow: 0   \ 1;__
- 超出主轴方向（缩小）0不做缩小
flex-thrink: 0   \ 1; 
- 缩写 flex-grow flex-shrink flex-basis 
flex:1 1 auto; 平均分配