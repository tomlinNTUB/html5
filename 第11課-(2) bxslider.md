# 第11課 jQuery 外掛


## (2) bxslider


##### 執行結果:
![GitHub Logo](/imgs/results11-2.jpg)


##### 下載網址
```
https://github.com/stevenwanderski/bxslider-4
```



##### 引用官網外掛檔案
```
   |___<dist>
         |___ <images>
         |       |_(圖片檔)
         |        
         |___ jquery.bxslider.css
         |___ jquery.bxslider.js
```



##### 檔案放置方式:
```
**以第10課-(2)的網頁為基礎, 增加以下:

   | 
   |___<images>
   |     |___ p01-slider.jpg   (尺寸:800px*400px)
   |     |___ p02-slider.jpg   (尺寸:800px*400px)
   |     |___ p03-slider.jpg   (尺寸:800px*400px)
   |     |___ (官網提供的圖片檔)   
   |     
   |___<css>
   |     |___ jquery.bxslider.css (由官網複製)
   |     |___ my.jquery.bxslider.css (自行增加) 
   |
   |___<js>
   |     |___ jquery.bxslider.js (由官網複製)    
   |     |___ my.jquery.bxslider.js (自行增加)     
   |
   |___index.html(增加顯示區域)  
```



##### 檔案名稱: css/my.jquery.bxslider.css
```css
@charset "utf-8";

.bx-wrapper .bx-loading {
    background: url(../images/bx_loader.gif) center center no-repeat #ffffff;
}

.bx-wrapper .bx-prev {
    background: url(../images/controls.png) no-repeat 0 -32px;
}

.bx-wrapper .bx-next {
    background: url(../images/controls.png) no-repeat -43px -32px;
}

.bx-wrapper .bx-controls-auto .bx-start {
    background: url(../images/controls.png) -86px -11px no-repeat;
}

.bx-wrapper .bx-controls-auto .bx-stop {
    background: url(../images/controls.png) -86px -44px no-repeat;
}
```



##### 檔案名稱: js/my.jquery.bxslider.js
```js
$(document).ready(function(){
    $('.bxslider').bxSlider();
});
```



##### 檔案名稱: index.html(引用外掛)  
```html
.
. (加入css)
<link href="css/jquery.bxslider.css" rel="stylesheet" type="text/css" />
<link href="css/my.jquery.bxslider.css" rel="stylesheet" type="text/css" />
.
.
.
. (加入js)
<script src="js/jquery.bxslider.js"></script>   
<script src="js/my.jquery.bxslider.js"></script> 
```



##### 檔案名稱: index.html(增加顯示區域)  
```html
<!--~~~~~~~~~~~~~~~~-->
<!-- bxslider 測試  -->
<!--~~~~~~~~~~~~~~~~-->
<p>        
    <ul class="bxslider">
        <li><img src="images/p01-slider.jpg" /></li>
        <li><img src="images/p02-slider.jpg" /></li>
        <li><img src="images/p03-slider.jpg" /></li>
        <li><img src="images/p04-slider.jpg" /></li>
    </ul>
</p>
<!--~~~~~~~~~~~~~~~~--> 
```
