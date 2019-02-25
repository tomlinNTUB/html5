# 12-7 使用jQuery外掛-mixitup

### 練習重點
```
使用jQuery外掛, 增加網頁特殊功能.
```

### 執行結果:
![GitHub Logo](/imgs/results12-7.jpg)


### 外掛網址
```
https://github.com/patrickkunka/mixitup
```

### 引用官網外掛檔案
```
   |__ <dist>
   |      |__ mixitup.js
   |
   |__ <demos>
          |__ <basic>   
                 |__ style.css
```


### 檔案放置方式 (以11-3範例為基礎, 增修以下):
```
   |__ index.html  (引用外掛, 增加顯示區域) 
   |  
   |__ <imgs>
   |     |__ p01-small.jpg   (200像素*200像素)
   |     |__ p02-small.jpg   (200像素*200像素)
   |     |__ p03-small.jpg   (200像素*200像素)
   |     |__ p04-small.jpg   (200像素*200像素)   
   |
   |__ <css>
   |     |__ style.css       (由官網複製, **需修改) 
   |     |__ my.mixitup.css  (自行增加)    
   |
   |__ <js>
         |__ mixitup.js      (由官網複製)     
         |__ my.mixitup.js   (自行增加) 
```


### (1) style.css
``` css
將其中所有 .container 改成 .container_mixitup
(共改2個)
```

### (2) my.mixitup.css
``` css
@charset "utf-8";

/* 設定卡片寬度 */
.mix,
.gap {
    width: 170px;
    background:#eee;
}

/* 設定卡片上方分類顏色 */
.mix {
    border:none;
    border-top: 15px solid currentColor;
    box-shadow:0px 0px 5px 1px #000;
}

/* 設定卡片高度 */
.mix:before {
    padding-top: 160px;
}

/* 設定按鈕背景 */
p.controls{
    background-color:#fff;
}

/* 設定按鈕文字 */
p.controls a{
    font-size:16px;
    color:#666;
    margin-right:20px;
    cursor:pointer;
}

/* 設定按鈕點擊後 */
.mixitup-control-active {
    background: transparent;
}

/* 自訂標題顏色 */
.mix.darkRed {
    color: #550000;
}

.mix.middleRed {
    color: #aa3939;
}

.mix.lightRed {
    color: #ffaaaa;
}
```

### (3) my.mixitup.js
``` js
$(function(){
    var containerEl = document.querySelector('.container');
    var mixer = mixitup(containerEl);
})
```


### (4) index.html (引用外掛)  
``` html
.
.
(加入css)
<link href="css/style.css" rel="stylesheet" />
<link href="css/my.mixitup.css" rel="stylesheet" />
.
.
.
.
(加入js)
<script src="js/mixitup.js"></script> 
<script src="js/my.mixitup.js"></script>   
.
.
```

### (5) index.html (增加顯示區域)  
``` html
<!--~~~~~~~~~~~~~~~~~~-->
<!-- mixitup 測試     -->
<!--~~~~~~~~~~~~~~~~~~-->
<p class="controls">
    <a data-filter="all">全部</a>
    <a data-filter=".darkRed">深紅</a>
    <a data-filter=".middleRed">中紅</a>
    <a data-filter=".lightRed">淺紅</a>
</p>

<div class="container_mixeditup">
    <div class="mix darkRed" style="background:url(imgs/p01-small.jpg)"></div>
    <div class="mix darkRed" style="background:url(imgs/p02-small.jpg)"></div>
    <div class="mix middleRed" style="background:url(imgs/p03-small.jpg)"></div>
    <div class="mix lightRed" style="background:url(imgs/p04-small.jpg)"></div>

    <div class="gap"></div>
    <div class="gap"></div>
    <div class="gap"></div>
</div>
<!--~~~~~~~~~~~~~~~~~~--> 
```
