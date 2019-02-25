# 12-3 使用jQuery外掛-tinytip

### 練習重點
```
使用jQuery外掛, 增加網頁特殊功能.
```

### 執行結果:
![GitHub Logo](/imgs/results12-3.jpg)


### 外掛網址
```
https://github.com/Sweefty/tinytip
```

### 引用官網外掛檔案
```
   |__ tinytip.js   
```


### 檔案放置方式 (以11-3範例為基礎, 增修以下):
```
   |__ index.html  (引用外掛, 增加顯示區域) 
   |    
   |__ <imgs>
   |     |__ p01-small.jpg   (250像素*150像素)
   |
   |__ <css>
   |     |__ my.tinytip.css  (自行增加) 
   |
   |__ <js>
         |__ tinytip.js     (由官網複製)     
         |__ my.tinytip.js  (自行增加)       
```


### (1) my.tinytip.css
``` css
@charset "utf-8";

/* 可點擊的項目 */
.element{
    cursor:pointer;	
    border-bottom:1px dotted #333;	
}

/*  項目中的圖片 */
.tinytip img{
    vertical-align:middle;
    box-shadow:0px 0px 10px 1px #000;	
    border-radius:10px;
}
```

### (2) my.tinytip.js
``` js
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

### (3) index.html (引用外掛)  
``` html
.
.
(加入css)
<link href="css/my.tinytip.css" rel="stylesheet" />
.
.
.
.
(加入js)
<script src="js/tinytip.js"></script> 
<script src="js/my.tinytip.js"></script> 
.
.
```

### (4) index.html (增加顯示區域)  
``` html
<!--~~~~~~~~~~~~~~~~~~-->
<!-- tinytip 測試     -->
<!--~~~~~~~~~~~~~~~~~~-->
<span class="element">蔣勳</span>
<!--~~~~~~~~~~~~~~~~~~--> 
```
