---
layout: post
title: 「从零开始」做一个 FlappyBird 那样的游戏 第4节 - 课后挑战：戴上帽子
date: '2016-01-23 14:44:49'
tags:
- flappybird
---


本文相关视频：[网易云课堂](http://study.163.com/course/courseLearn.htm?courseId=1685005&lessonId=1003157048)

## 挑战内容

1. 给游戏的主角头上戴上一顶帽子。
2. 在每次主角飞跳的时候，让这个帽子在 0.15 秒的时间内向上移动 12 个像素，然后再同样的时间内落回到头上。（时间模式选择`EaseInEaseOut`）

![](/content/images/2016/01/L4-challenge-part-1-1.png)


## 提示
1. 帽子的图片名为 `Sombrero`。
2. 将帽子做为主角的子元素加入到主角的下面 - `主角.addChild(帽子)`
3. 移动帽子的时机应该是和主角飞跳时是一起的。
4. 当你完成向上移动的动作时，使用 `.reversedAction()`这个方法就可以得到反向的动作。
5. 每一个`SKAction`动作都可以指定一个`timingMode`（时间模式）来设置它的动作时间函数，`EaseInEaseOut`就是其中一种，可以理解成「淡入淡出」。
6. 需要用到动作队列 - `SKAction.sequence([...])`

## 更多提示？

暂时还没想到... Sorry ＝＝

## 答案
参见 [第 4 节课完成挑战代码](https://github.com/FangYiXiong/FlappyZoe/archive/part4-challenge-finished.zip)。