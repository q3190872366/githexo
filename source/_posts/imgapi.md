---
title: 随机图API
categories: PHP
tags: [API, PHP]
index_img: http://cpblog.cn/api/img/api.php
date: 2021-9-1 13:37:19 

---

[Wallpaper Abyss](https://wall.alphacoders.com/)

[Awesome Wallpapers](https://wallhaven.cc/)

[WallpapersWide.com](http://wallpaperswide.com/)

图片压缩网站[TinyPNG](https://tinypng.com/)

创建一个img.txt和一个random.php

如何一件复制你上传图片的url呢，如果你使用的是PicGo上传的话，可以在“相册”一栏里，选择你想要的图片，然后一件复制url

```php
<?php
//存有image链接的文件名img.txt
$filename = "img.txt";
if(!file_exists($filename)){
    die('文件不存在');
}
 
//从文本获取链接
$pics = [];
$fs = fopen($filename, "r");
while(!feof($fs)){
    $line=trim(fgets($fs));
    if($line!=''){
        array_push($pics, $line);
    }
}
 
//从数组随机获取链接
$pic = $pics[array_rand($pics)];
 
//返回指定格式
$type=$_GET['type'];
switch($type){
 
//JSON返回
case 'json':
    header('Content-type:text/json');
    die(json_encode(['pic'=>$pic]));
 
default:
    die(header("Location: $pic"));
}
?>
```

