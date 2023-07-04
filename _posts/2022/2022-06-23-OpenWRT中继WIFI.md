---
id: 49
title: OpenWRT中继WIFI
date: '2022-06-23T14:50:21+08:00'
author: yexca
layout: post
guid: 'https://yexca.xyz/?p=771'
permalink: /archives/49
argon_hide_readingtime:
    - 'false'
argon_meta_simple:
    - 'false'
argon_first_image_as_thumbnail:
    - default
argon_show_post_outdated_info:
    - default
argon_after_post:
    - ''
argon_custom_css:
    - ''
views:
    - '256'
categories:
    - 日常
tags:
    - OpenWRT
---

# 引言

今日尝试了一下之前试过的无线中继，发现已经不会了，果然做一项东西还是要写个文章记录一下比较好啊

本文中，将OpenWRT路由器连接的WIFI称为上级路由，OpenWRT路由器称为路由器

# 前提

确保路由器与上层路由的LAN口地址(即进入路由器后台的地址)不可与上级路由一致，如一致将无法上网

## 修改路由器LAN口地址

进入路由器后台的`网络`-`接口`，点击`LAN`的`修改`，改变其`IPv4地址`即可

例如上级路由后台地址为`192.168.1.1`，路由器可改为`192.168.5.1`

修改完并`保存&应用`后在浏览器输入修改后的地址访问路由器后台

# 路由器连接WIFI

进入`网络`-`无线`，点击`扫描`，找到要连接的WIFI，点击`加入网络`，输入网络名称与密码，点击`提交`，然后点击`保存&应用`即可

# 路由器开WIFI

如果路由器有2.4G和5G双频段，可以选择与上一步不同频段创建WIFI，这样兼容性最好 （如果另一个频段已经有一个WIFI，可能已经能用啦）

如果只有单频段，则在相同频段新建一个，必须要新建，可能不会成功，毕竟有些路由器不支持单网卡同时入和出

开WIFI和普通流程一样，在`网络`-`无线`处添加，输入SSID(即WIFI名称)和密码然后`保存&应用`即可

# 参考文章

[OpenWrt进阶教程之无线中继配置指南 - 爱一枝梅](https://iyzm.net/openwrt/512.html)