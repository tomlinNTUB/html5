# 12-4 使用jQuery外掛-bxslider

### 練習重點
```
使用jQuery外掛, 增加網頁特殊功能.
```

### 執行結果:
![GitHub Logo](/imgs/results12-4.jpg)


### 外掛網址
```
https://github.com/stevenwanderski/bxslider-4
```

### 引用官網外掛檔案
```
   |__ <dist>
         |__ <images>
         |      |__ bx_loader.gif
         |      |__ controls.png      
         |        
         |__ jquery.bxslider.css
         |__ jquery.bxslider.js 
```


### 檔案放置方式 (以11-3範例為基礎, 增修以下):
```
   |__ index.html  (引用外掛, 增加顯示區域) 
   |    
   |__ <imgs>
   |     |__ p01-slider.jpg   (800像素*400像素)
   |     |__ p02-slider.jpg   (800像素*400像素)
   |     |__ p03-slider.jpg   (800像素*400像素)
   |     |__ p04-slider.jpg   (800像素*400像素)
   |     |__ bx_loader.gif    (由官網複製)
   |     |__ controls.png     (由官網複製)
   |
   |__ <css>
   |     |__ jquery.bxslider.css  (由官網複製) 
   |
   |__ <js>
         |__ jquery.bxslider.js     (由官網複製)     
         |__ my.jquery.bxslider.js  (自行增加)       
```


### (1) my.jquery.bxslider.js
``` js
$(document).ready(function(){
    $('.bxslider').bxSlider();
});
```

### (2) index.html (引用外掛)  
``` html
.
.
(加入css)
<link href="css/jquery.bxslider.css" rel="stylesheet" />
.
.
.
.
(加入js)
<script src="js/jquery.bxslider.js"></script>   
<script src="js/my.jquery.bxslider.js"></script> 
.
.
```

### (3) index.html (增加顯示區域)  
``` html
<!--~~~~~~~~~~~~~~~~-->
<!-- bxslider 測試  -->
<!--~~~~~~~~~~~~~~~~-->
<p>        
    <ul class="bxslider">
        <li><img src="imgs/p01-slider.jpg" /></li>
        <li><img src="imgs/p02-slider.jpg" /></li>
        <li><img src="imgs/p03-slider.jpg" /></li>
        <li><img src="imgs/p04-slider.jpg" /></li>
    </ul>
</p>
<!--~~~~~~~~~~~~~~~~--> 
```
