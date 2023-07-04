---
id: 3
title: WordPress嵌入BiLiBiLi视频说明
date: '2021-11-06T16:43:20+08:00'
author: yexca
layout: post
guid: 'http://47.98.189.51/?p=108'
permalink: /archives/3
um_content_restriction:
    - 'a:8:{s:26:"_um_custom_access_settings";b:0;s:14:"_um_accessible";i:0;s:28:"_um_access_hide_from_queries";b:0;s:19:"_um_noaccess_action";i:0;s:30:"_um_restrict_by_custom_message";i:0;s:27:"_um_restrict_custom_message";s:0:"";s:19:"_um_access_redirect";i:0;s:23:"_um_access_redirect_url";s:0:"";}'
views:
    - '201'
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
categories:
    - 网站建设
tags:
    - WordPress
---

首先到待嵌入的视频将鼠标移到分享按钮上（不用点击）

然后移到嵌入代码并复制

（本例代码如下）

```html

<iframe src="//player.bilibili.com/player.html?aid=583631611&bvid=BV1Tz4y1X7Bg&cid=206708397&page=1" scrolling="no" border="0" frameborder="no" framespacing="0" allowfullscreen="true"> </iframe>

```

我们需要这串代码中的”**aid**“和”**cid**“部分（即 aid=583631611 和 cid=206708397 ）

然后将aid和cid填入下方代码的相应位置

```html

<div style="position: relative; padding: 30% 45%;">
<iframe style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;" src="https://player.bilibili.com/player.html?cid=206708397&aid=583631611&page=1&as_wide=1&high_quality=1&danmaku=0" frameborder="no" scrolling="no"></iframe>
</div>

```

（以上代码中aid和cid已替换）

在编写文章的过程若插入视频只需将区块设成“**自定义HTML**”然后把替换好aid和cid的代码拷贝过去即可

如下为示例视频

<div style="position: relative; padding: 30% 45%;"><iframe frameborder="no" scrolling="no" src="https://player.bilibili.com/player.html?cid=206708397&aid=583631611&page=1&as_wide=1&high_quality=1&danmaku=0" style="position: absolute; width: 100%; height: 100%; left: 0; top: 0;"></iframe></div>

参考[王陸](https://www.cnblogs.com/wkfvawl/)大佬的文章[关于博客园内嵌入bilibili视频](https://www.cnblogs.com/wkfvawl/p/12268980.html)