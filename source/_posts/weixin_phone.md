---
title: 微信语音/视频通话定位
tags: 
- 漏洞
categories:
- 技术分享
top_img: /img/yangb.png
cover: /img/CVE.png
---

通过测试发现微信语音/视频通话能够定位到对方的位置.

使用电脑无线网卡共享无线网络, 手机连接至电脑WIFI, 使用wireshark抓包,微信语音视频通话通过UDP协议, 因此我们用`ip.addr == 手机IP地址 && udp`表达式来过滤数据包,语音电话接通之后会大量的数据包刷出来,通过IP反查即可获取到对方的地理位置. 

> IP精确定位网站 <https://www.chaipip.com/aiwen.html>

动态IP定位比较模糊, 静态IP定位更加准确, 因此如果对方连接的是公共wifi, 定位就很精确. 例如连接到网吧WIFI, 就可以查出网吧的地址名称.