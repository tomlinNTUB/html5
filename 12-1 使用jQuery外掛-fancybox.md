# 12-1 使用jQuery外掛-fancybox

### 練習重點
```
使用jQuery外掛, 增加網頁特殊功能.
```

### 執行結果:
![GitHub Logo](/imgs/results12-1.jpg)


### 下載網址
```
https://github.com/fancyapps/fancyBox
```

### 引用官網外掛檔案
```
   |___<dist>
         |___ jquery.fancybox.css
         |___ jquery.fancybox.js
```

### 檔案放置方式:
```
**以11-3為基礎, 增加以下:

   |__ index.html(增加顯示區域) 
   |
   |__ <imgs>
   |     |__ p01-big.jpg     (尺寸:800px*600px)
   |     |__ p01-small.jpg   (尺寸:200px*200px)
   |     |__ p02-big.jpg     (尺寸:800px*600px)
   |     |__ p02-small.jpg   (尺寸:200px*200px)
   |     |__ p03-big.jpg     (尺寸:800px*600px)
   |     |__ p04-small.jpg   (尺寸:200px*200px)   
   |     
   |__ <css>
   |     |__ jquery.fancybox.css    (由官網複製)
   |     |__ my.jquery.fancybox.css (自行增加) 
   |
   |__ <js>
         |__ jquery.fancybox.js    (由官網複製)     
  
```


### (1) my.jquery.fancybox.css
``` css
@charset "utf-8";

p.imageView img{
    box-shadow:0px 0px 5px 1px #000;
    margin-right:20px;
}

p.imageView a{
    outline:none;
    float:left;
}

p.imageView:after{
    content: '';
    display: block;
    clear: both;
}
```


### (2) index.html (引用外掛)  
``` html
.
. (加入css)
<link href="css/jquery.fancybox.css" rel="stylesheet" type="text/css" />
<link href="css/my.jquery.fancybox.css" rel="stylesheet" type="text/css" />
.
.
.
. (加入js)
<script src="js/jquery.fancybox.js"></script> 
```

### (3) index.html (增加顯示區域)  
``` html
<!--~~~~~~~~~~~~~~~~-->
<!-- Fancybox 測試  -->
<!--~~~~~~~~~~~~~~~~-->
<p class="imageView">
    <a data-fancybox="gallery" href="imgs/p01-big.jpg">
        <img src="imgs/p01-small.jpg">
    </a>
                
    <a data-fancybox="gallery" href="imgs/p02-big.jpg">
        <img src="imgs/p02-small.jpg">
    </a> 
                
    <a data-fancybox="gallery" href="imgs/p03-big.jpg">
        <img src="imgs/p03-small.jpg">
    </a>                     
</p>
<!--~~~~~~~~~~~~~~~~--> 
```
