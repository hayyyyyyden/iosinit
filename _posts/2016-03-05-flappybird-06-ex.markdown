---
layout: post
title: 「从零开始」做一个 FlappyBird 那样的游戏 第6节 课后挑战：重新开始游戏
date: '2016-03-05 16:16:13'
---


原文地址：[「从零开始」做一个 FlappyBird 那样的游戏 第6节 - 课后挑战：戴上帽子](http://iosinit.com/flappybird-06-ex/)

本文相关视频：[网易云课堂](http://study.163.com/course/courseLearn.htm?courseId=1685005&lessonId=1003227002)

## 挑战内容

1. 当游戏进入「显示分数」的状态后，用户点击屏幕，游戏重新开始
2. 通过新建一个游戏场景`GameScene`，并切换到这个新的游戏场景来实现。
3. 当切换新游戏的时候播放一个`砰的音效`。

![screenShot-6-1](http://7xqycx.com1.z0.glb.clouddn.com/2016-03-06-screenShot-6-1.png)

## 提示
1. 砰的音效的文件名为 `Pop.wav`。
2. 如何新建一个新的游戏场景？相关代码可以在`GameViewController.swift`这个文件的`viewWillLayoutSubeViews`方法里找到，或参见第一节的视频。

3. 一旦你创建好了新的场景，切换到新的游戏场景用到的方法名字是`view.presentScene()`，它有个可选的参数，允许你增加转换场景时的特效`SKTransion`。
	
	如果你选用带特效参数的那个，请要注意创建特效时的持续时间（`duration`）参数，不要太大！不然可能会遇到让你恼火的 Bug..（你做的时候就会知道我说的是什么了。）。

## 参考解答

参见 [第 6 节课完成挑战后的代码](https://github.com/FangYiXiong/FlappyZoe/archive/part-6-challenge-finished.zip)。

或者，这次新添加的 [解答视频](http://study.163.com/course/courseLearn.htm?courseId=1685005&lessonId=1003227008)。

当然，还是我还是建议你先根据提示去完成挑战，遇到困难时再参考答案，毕竟这个挑战作业不计分，也没有人会去检查。
