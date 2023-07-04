---
id: 2
title: WordPress限制用户访问媒体库
date: '2021-11-06T14:31:04+08:00'
author: yexca
layout: post
guid: 'http://47.98.189.51/?p=30'
permalink: /archives/2
um_content_restriction:
    - 'a:8:{s:26:"_um_custom_access_settings";b:0;s:14:"_um_accessible";i:0;s:28:"_um_access_hide_from_queries";b:0;s:19:"_um_noaccess_action";i:0;s:30:"_um_restrict_by_custom_message";i:0;s:27:"_um_restrict_custom_message";s:0:"";s:19:"_um_access_redirect";i:0;s:23:"_um_access_redirect_url";s:0:"";}'
views:
    - '204'
categories:
    - 网站建设
tags:
    - WordPress
---

默认情况下，WordPress允许作者​​查看您网站媒体库中的所有图像。允许作者查看媒体库中的所有文件。 他们还可以查看由管理员 ， 编辑或其他作者上传的图像。

对于许多网站而言，这可能并不重要。 但是，如果您运行一个多作者网站 ，则可能需要更改它。

首先，进入 “网站根目录/wp-content/themes/您当前使用的主题名称/”

找到functions.php文件并编辑，在末尾插入如下代码即可

```php

// Limit media library access
 
add_filter( 'ajax_query_attachments_args', 'wpb_show_current_user_attachments' );
 
function wpb_show_current_user_attachments( $query ) {
    $user_id = get_current_user_id();
    if ( $user_id && !current_user_can('activate_plugins') && !current_user_can('edit_others_posts
') ) {
        $query['author'] = $user_id;
    }
    return $query;
}

```

参考文章：[如何限制媒体库对WordPress中用户自己上传的内容的访问](https://blog.csdn.net/cumohuo9136/article/details/108609313)