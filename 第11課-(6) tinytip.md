# 第11課 jQuery 外掛


## (6) tinytip


##### 執行結果:
![GitHub Logo](/imgs/results11-6.jpg)


##### 下載網址
```
https://github.com/Sweefty/tinytip
```



##### 引用官網外掛檔案
```
   |___tinytip.js                  
```



##### 檔案放置方式:
```
**以第10課-(2)的網頁為基礎, 增加以下:
   
   |
   |___<images>
   |     |___ p01-small.jpg   (尺寸:250px*150px)
   |     
   |___<css>
   |     |___ my.tinytip.css  (自行增加) 
   |
   |___<js>
   |     |___ tinytip.js      (由官網複製)
   |     |___ my.tinytip.js   (自行增加)     
   |
   |___index.html(增加顯示區域)  
```



##### 檔案名稱: css/my.tinytip.css
```css
@charset "utf-8";

.element{
    cursor:pointer;	
    border-bottom:1px dotted #333;	
}


.tinytip img{
    vertical-align:middle;
    box-shadow:0px 0px 10px 1px #000;	
    border-radius:10px;
}
```



##### 檔案名稱: js/my.tinytip.js
```js
$('.element').tinytip({
    tooltip : '<img src="images/p01-small.jpg">',
    position : 'bottom',
    animation : {
        top : -10
    },
    fix : {
        top: 10,
        left: -5
    },
    speed : 100,
    on : 'click',
    off: 'click',
    preventClose : true,
    onLoad : function(e){}
});
```



##### 檔案名稱: index.html(引用外掛)  
```html
.
. (加入css)
<link href="css/my.tinytip.css" rel="stylesheet" type="text/css" />
.
.
.
. (加入js)
<script src="js/tinytip.js"></script> 
<script src="js/my.tinytip.js"></script>      
```



##### 檔案名稱: index.html(增加顯示區域)  
```html
<!--~~~~~~~~~~~~~~~~~~-->
<!-- tinytip 測試     -->
<!--~~~~~~~~~~~~~~~~~~-->
<span class="element">蔣勳</span>
<!--~~~~~~~~~~~~~~~~~~--> 
```
