# 第11課 jQuery 外掛


## (5) Mixitup


##### 執行結果:
![GitHub Logo](/imgs/results11-5.jpg)


##### 下載網址
```
https://github.com/patrickkunka/mixitup
```



##### 引用官網外掛檔案
```
   |___<dist>
   |      |___ mixitup.js
   |
   |___<demos>
          |___ <basic>   
                  |___ style.css
                  |___ index.html (參考外掛用法)                  
```



##### 檔案放置方式:
```
**以第10課-(2)的網頁為基礎, 增加以下:
   
   |
   |___<images>
   |     |___ p01-small.jpg   (尺寸:200px*200px)
   |     |___ p02-small.jpg   (尺寸:200px*200px)
   |     |___ p03-small.jpg   (尺寸:200px*200px)
   |     |___ p04-small.jpg   (尺寸:200px*200px)   
   |     
   |___<css>
   |     |___ style.css       (由官網複製, **需修改**)
   |     |___ my.mixitup.css  (自行增加) 
   |
   |___<js>
   |     |___ mixitup.js      (由官網複製)
   |     |___ my.mixitup.js   (自行增加)     
   |
   |___index.html(增加顯示區域)  
```



##### 檔案名稱: css/style.css
```
將其中所有 .container 改成 .container_mixitup
```



##### 檔案名稱: css/my.mixitup.css
```css
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


##### 檔案名稱: js/my.mixitup.js
```js
$(function(){
    var containerEl = document.querySelector('.container');
    var mixer = mixitup(containerEl);
})
```



##### 檔案名稱: index.html(引用外掛)  
```html
.
. (加入css)
<link href="css/style.css" rel="stylesheet" type="text/css" />
<link href="css/my.mixitup.css" rel="stylesheet" type="text/css" />
.
.
.
. (加入js)
<script src="js/mixitup.js"></script> 
<script src="js/my.mixitup.js"></script>     
```



##### 檔案名稱: index.html(增加顯示區域)  
```html
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
    <div class="mix darkRed" style="background:url(images/p01-small.jpg)"></div>
    <div class="mix darkRed" style="background:url(images/p02-small.jpg)"></div>
    <div class="mix middleRed" style="background:url(images/p03-small.jpg)"></div>
    <div class="mix lightRed" style="background:url(images/p04-small.jpg)"></div>

    <div class="gap"></div>
    <div class="gap"></div>
    <div class="gap"></div>
</div>
<!--~~~~~~~~~~~~~~~~~~--> 
```
