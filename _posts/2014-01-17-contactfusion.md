---
date: 2014-01-17 22:33:17+00:00
layout: post
title: 完美控专用：CeleDial 联系人整理功能介绍
categories: 文档
tags: 分享 iOS
---

在 [CeleDail for iPhone](http://www.celedial.com/appstore) 的设置界面中，提供了一系列非常有用的整理联系人数据的小功能：

![](/assets/ContactFusion.png)

1). 在多个Google、iCloud、Hotmail账户之间同步联系人：使用之前在系统设置中添加多个联系人账户即可，然后在CeleDial设置中，点击所有联系人群组，在下面展开的单个联系人账号的右侧点击有命令可以操作。目前仅支持单向同步。 

2). 电话号码批量添加国家区号（如+86）：8个数字以上的才会添加，区号是根据区域设置来的，中国+86，已经有+或00开头的，不会添加。会自动删除“-”和“ ”（空格）。 

3). 批量删除国家区号(如+86)。 

4). 批量合并姓氏和名字。 

5). 批量拆分姓氏和名字：仅拆分2、3、4个非英文字母的姓名，或者带空格的英文姓名，拆分和合并可以轮着用，整理得更透彻。 

<!-- more -->

6). 把未分组的联系人添加到“未分组”中（以便整理）：仅支持 CardDAV/Local/iCloud 账户，推荐iCloud分组，可以同步到 iCloud上来管理分组。Exchange不支持分组，iOS的设计如此。Google 已经支持 CardDAV，但Google 竟然不支持同步分组（不过跟 CeleDial 没关系）。 

iOS SDK 不支持读取联系人账户的名称，只能读取类型，更悲催的是iCloud类型的联系人，实际上也是CardDAV，所以没法很好地来标识联系人来源，再次提请注意：请确认操作不会造成联系人数据丢失！！ 

最好是在iPhone中，关闭掉网络，然后使用后，检查一下联系人没问题，再打开网络同步到网上。 

注意：风险自负，仅供完美主义者或强迫症专用！！！：）

这些功能在一年前的 CeleDial 2.4 开始已提供了，如果需要可在 AppStore 中 [下载 CeleDial](http://www.celedial.com/appstore)。

想在各大在线联系人账户之前迁移的用户，终于有解决方案了，操起手中的肾机开干吧！