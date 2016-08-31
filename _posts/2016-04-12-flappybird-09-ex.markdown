---
layout: post
title: 「从零开始」做一个 FlappyBird 那样的游戏 第9节 课后挑战：起飞！
date: '2016-04-12 10:14:00'
---


原文地址：[「从零开始」做一个 FlappyBird 那样的游戏 第9节 - 课后挑战：起飞！](http://iosinit.com/flappybird-09-ex/)

## 挑战内容

1. 在教程状态下，让主角不停地上下移动，速度为每 0.4 秒移动 50 个像素。

2. 给主角增加扇动翅膀的动画。

![](/content/images/2016/04/flappybird-09-finished-demo-1.gif)

## 提示
1. 第 1 项挑战和第 4 节课后的挑战很相似，可以参考当时的[文档](http://iosinit.com/flappybird-04-ex/)。

2. 在「教程」状态下添加完动画之后，记得要在游戏状态时把动画移除，不然会发生奇怪的事情，你可以试试。

3. 扇动翅膀的原理就是在我们的图片资源中有 4 张主角的图片（bird0,bird1,bird2,bird3），每张翅膀的角度稍有不同，我们不断地更换这些图片就可以做到扇动翅膀的动画的效果了。

    ![](/content/images/2016/04/4sprites.png)

    在这里，我们需要用到 `SKAction.animateWithTextures([SKTexture], timePerFrame: )` 这个方法，第二个参数决定了扇动翅膀的快慢，给一个你觉得合适的时间就可以了。第一个参数要求一个 `SKTexture` 类型的数组，如果你不清楚如何做，尝试下面的代码：

        var 角色贴图组: Array<SKTexture> = []
        
        for i in 0..<k角色动画总帧数 {
            角色贴图组.append(SKTexture(imageNamed: "Bird\(i)"))
        }
        
        for i in (k角色动画总帧数-1).stride(through: 0, by: -1) {
            角色贴图组.append(SKTexture(imageNamed: "Bird\(i)"))
        }
 其中，`k角色动画总帧数` 是需要新定义的一个常量，在我们这个例子中就是`4`。
 
4. 扇动翅膀的动画不需要停止，我们甚至可以让它从「主菜单」的时候就开始运行。

## 参考解答

参见 [第 9 节课完成挑战后的代码](https://github.com/FangYiXiong/FlappyZoe/archive/part-9-challenge-finished.zip)。
