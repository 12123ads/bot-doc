---
id: bilibili
title: 哔哩哔哩
---

## B站视频解析

哔哩哔哩直接分享视频到群聊/私聊即可触发视频解析，返回视频

> 源插件链接：[bilibili视频链接解析](https://www.npmjs.com/package/koishi-plugin-bilibili-videolink-analysis/v/0.5.1)
## B站推送

登录B站：进行任何操作前，请先登录B站
- 使用指令 `bili login` 获取登录二维码，使用B站扫码登录
订阅UP主：订阅你想要推送的UP主
- 使用指令 `bili sub <uid> [Q群号]` 订阅需要订阅的UP主
- 参数说明：
  - `uid` 为必填参数，为 `up主` 的  `uid` 
  - `Q群号` 为可选参数，可以添加多个，如果Q群号为 `all` 则会向机器人加入的所有群聊推送
- 选项说明：`bili sub <uid>` 有两个选项：-l 和 -d
  - `-l` 为订阅UP主直播间，包括直播开播通知，定时推送直播内容，下播通知
  - `-d` 为订阅UP主动态推送，目前实现推送的动态类型有：普通图文动态，转发动态，直播预约动态
- 例如：
  - `bili sub 1194210119 ` 订阅UID为1194210119的UP主
  - `bili sub 1194210119 -d` 订阅UID为1194210119的UP主动态推送
  - `bili sub 1194210119 -ld` 订阅UID为1194210119的UP主动态推送和直播间
  - `bili sub 1194210119 1234567 2345678` 订阅UID为1194210119的UP主，向Q群号为1234567和2345678两个群进行推送
  - `bili sub 1194210119 all` 订阅UID为1194210119的UP主，向机器人加入的所有群聊进行推送
- Tips:
  - 除非使用指令 `bili sub 1194210119 -ld` ，没有加选项或只加了一个选项的指令都会再次询问是否需要订阅另一项。例如：使用指令 `bili sub 1194210119 -d` 机器人会询问是否需要订阅直播间
  - `[Q群号]` 这个可选参数仅支持Q群
取消订阅UP主：取消订阅不需要推送的UP主
- 使用指令 `bili unsub <uid>` 取消订阅不需要订阅的UP主
- 参数说明：`uid` 为必填参数，为 `up主` 的 `uid`
- 选项说明：`bili unsub <uid>` 有两个选项：-l 和 -d
  - `-l` 为取消订阅UP主直播间
  - `-d` 为取消订阅UP主动态
- 例如：
  - `bili unsub 123456` 取消订阅UID为123456的UP主动态推送和直播间
  - `bili unsub 123456 -d` 取消订阅UID为123456的UP主动态推送
  - `bili unsub 123456 -dl` 取消订阅UID为123456的UP主动态推送和直播间
查看目前已订阅的UP主：
- 使用指令 `bili show`

> 原插件链接：[B站推送](https://www.npmjs.com/package/koishi-plugin-bilibili-notify)