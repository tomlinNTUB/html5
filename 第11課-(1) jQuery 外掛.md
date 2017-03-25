# 第11課 jQuery 外掛


## (1) fancybox


##### 執行結果:
![GitHub Logo](/imgs/results11-1.jpg)


##### 下載網址
```
https://github.com/fancyapps/fancyBox
```



##### 複製檔案
```
   |___<dist>
         |___ jquery.fancybox.css
         |___ jquery.fancybox.js
```



##### 檔案放置方式:
```
**以第10課-(2)的網頁為基礎, 增加以下.

   | 
   |___<images>
   |     |___ p01-big.jpg     (尺寸:800px*600px)
   |     |___ p01-small.jpg   (尺寸:200px*200px)
   |     |___ p02-big.jpg     (尺寸:800px*600px)
   |     |___ p02-small.jpg   (尺寸:200px*200px)
   |     |___ p03-big.jpg     (尺寸:800px*600px)
   |     |___ p04-small.jpg   (尺寸:200px*200px)   
   |     
   |___<css>
   |     |___ jquery.fancybox.css (由官網複製)
   |     |___ my.jquery.fancybox.css (自行增加) 
   |
   |___<js>
   |     |___ jquery.fancybox.js (由官網複製)     
   |
   |___index.html(增加顯示區域)  
```



##### 檔案名稱: css/my.jquery.fancybox.css
```css
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



##### 檔案名稱: index.html(引用外掛)  
```html
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



##### 檔案名稱: index.html(增加顯示區域)  
```html
<!------------------->
<!-- Fancybox 測試  -->
<!-------------------> 
<p class="imageView">
    <a data-fancybox="gallery" href="images/p01-big.jpg">
        <img src="images/p01-small.jpg">
    </a>
                
    <a data-fancybox="gallery" href="images/p02-big.jpg">
        <img src="images/p02-small.jpg">
    </a> 
                
    <a data-fancybox="gallery" href="images/p03-big.jpg">
        <img src="images/p03-small.jpg">
    </a>                     
</p>
<!-------------------> 
```
