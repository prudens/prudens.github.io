---
layout: post
title: 加入蜗牛游戏开发实时语音
author: prudens
---

转眼间，在新公司——苏州蜗牛游戏——已经过去了两个多月，整体氛围上比较轻松，不需要打卡，研发氛围浓厚，没有产品需求上的压力，大家做好语音这块就好。
目前团队不大，有两部分人，一部分做网络，SDN和CDN,貌似还在游戏视频直播这块的研究，另一部分就是我们，在做实时语音通信，一开始是
基于webrtc，那现在主要用底层的一些模块，比如adm, apm。想acm，amm和voe就不需要了。采用肖总自带的那一套引擎，不过我也没看到源码。
现在的webrtc的adm是采用jni的方式，播放和采集都调用Java库接口。这两天我们采用OpenELSE，都是C++代码，上层不需要传递一个jvm指针下
来。然后就是适配机型的问题，现在机子比较少，不好测试。

目前碰到的问题主要是调试的困难。比如除了bug不想windows有vs单步调试，全靠打印日志，定位问题很麻烦，而且编译库是在虚拟机里，每次
都要拷贝来拷贝去，后续可能会整理这个编译环境。然后争取这个月都搞定所有的事情，早日做好过年的准备。
