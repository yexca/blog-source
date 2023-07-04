---
id: 7
title: '关于在使用navicat连接SQL server的一些问题'
date: '2021-11-07T23:41:46+08:00'
author: hiyoung
layout: post
guid: 'http://47.98.189.51/?p=173'
permalink: /archives/7
um_content_restriction:
    - 'a:8:{s:26:"_um_custom_access_settings";b:0;s:14:"_um_accessible";i:0;s:28:"_um_access_hide_from_queries";b:0;s:19:"_um_noaccess_action";i:0;s:30:"_um_restrict_by_custom_message";i:0;s:27:"_um_restrict_custom_message";s:0:"";s:19:"_um_access_redirect";i:0;s:23:"_um_access_redirect_url";s:0:"";}'
views:
    - '200'
categories:
    - 数据库
---

在安装完SQL server和navicat后在navicat中添加数据库：

![](http://blog.yexca.xyz/wp-content/uploads/2021/11/AYXUL5D1LKZMP0FL.jpg)

1.连接名无要求，按照自己需要命名

2.打开安装好的SQL server 配置管理器

![](http://blog.yexca.xyz/wp-content/uploads/2021/11/86_J90MFSZUPY5K4PXG.jpg)
注意SQL Server（SQLEXPRESS）要保证在运行中，否则navicat无法连接  
双击打开后点击服务，可以看到自己的主机名

![](http://blog.yexca.xyz/wp-content/uploads/2021/11/M7_ALDIORM66MMVKHBLK.jpg)

3.此时打开navicat在主机的地方填上：主机名\\SQLEXPRESS(格式）

4.用户名填sa(为安装SQL server时的默认用户名，具体SQL server网上教程很多可以自己参考），密码是自己设置的（同样在SQL server安装时设置的密码）

5.测试连接成功即可使用

![](http://blog.yexca.xyz/wp-content/uploads/2021/11/O5L2Z62VUGGD1WLHA6.jpg)

注：仅个人在安装过程中遇到的问题，具体安装教程请参考网络

附上navicat 15及注册机：<https://pan.baidu.com/s/1cJ1EZ9Gyz6Jp6J03VqcDHA>

提取码：3n7g