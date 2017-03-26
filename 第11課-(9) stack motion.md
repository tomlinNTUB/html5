# 第11課 jQuery 外掛


## (9) stack motion hover effect


##### 執行結果:
![GitHub Logo](/imgs/results11-9.jpg)


##### 下載網址
```
https://github.com/codrops/StackMotionHoverEffects
```



##### 引用官網外掛檔案
```
   |___ <css> (複製資料夾及內容)  
   |
   |___ <js>  (複製資料夾及內容)  
   |
   |___ index.html (參考用法)   
```



##### 檔案放置方式:
```
**以第10課-(2)的網頁為基礎, 增加以下:

   |
   |___<images> 
   |     |___ p01-middle.jpg  (350px*350px)   
   |     |___ p02-middle.jpg  (350px*350px)  
   |     |___ p03-middle.jpg  (350px*350px)  
   |
   |___<css> (複製官網資料夾及內容) 
   |     |
   |     |___ my.anime.css  (自行增加)    
   |
   |___<js>  (複製官網資料夾及內容) 
   |     |
   |     |___ my.anime.css   (自行增加)     
   |
   |___index.html(增加顯示區域)  
```



##### 檔案名稱: css/my.anime.css
```css
body {
	color: #000;
}


/* 每個項目寬度 */
div.grid{
	width:240px;
	padding:0;
	margin-right:10px;
	float:left;
}

/* 圖片寬度 */
.grid__item{
	width:200px;		
}


/* 圖片高度 */
.stack {
	height: 150px;
}

/* 陰影顏色 */
.stack__deco {
	background-color: #000;
}
```



##### 檔案名稱: js/my.anime.js
```js
(function() {
    [].slice.call(document.querySelectorAll('.grid--effect-vega > .grid__item')).forEach(function(stackEl) {
        new VegaFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-castor > .grid__item')).forEach(function(stackEl) {
        new CastorFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-hamal > .grid__item')).forEach(function(stackEl) {
        new HamalFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-polaris > .grid__item')).forEach(function(stackEl) {
        new PolarisFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-alphard > .grid__item')).forEach(function(stackEl) {
        new AlphardFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-altair > .grid__item')).forEach(function(stackEl) {
        new AltairFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-rigel > .grid__item')).forEach(function(stackEl) {
        new RigelFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-canopus > .grid__item')).forEach(function(stackEl) {
        new CanopusFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-pollux > .grid__item')).forEach(function(stackEl) {
        new PolluxFx(stackEl);
    });
    [].slice.call(document.querySelectorAll('.grid--effect-deneb > .grid__item')).forEach(function(stackEl) {
        new DenebFx(stackEl);
    });
})();
```



##### 檔案名稱: index.html(引用外掛)  
```html
.
. (加入css)
<link rel="stylesheet" type="text/css" href="css/normalize.css" />
<link rel="stylesheet" type="text/css" href="css/demo.css" />		
<link rel="stylesheet" type="text/css" href="css/my.anime.css" />
.
.
.
. (加入js)
<script src="js/anime.min.js"></script>
<script src="js/main.js"></script>  
<script src="js/my.anime.min.js"></script>       
```



##### 檔案名稱: index.html(增加顯示區域)  
```html
<!--~~~~~~~~~~~~~~~~~~-->
<!-- t.js 測試        -->
<!--~~~~~~~~~~~~~~~~~~-->
<div class="grid grid--effect-hamal">
    <a href="#" class="grid__item grid__item--c1">
        <div class="stack">
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__figure">
                <img class="stack__img" src="images/p01-middle.jpg" alt="Image"/>
            </div>
        </div>
        <div class="grid__item-caption">
            <h3 class="grid__item-title"></h3>
        </div>
    </a>	
</div>

<div class="grid grid--effect-polaris">
    <a href="#" class="grid__item grid__item--c2">
        <div class="stack">
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__figure">
                <img class="stack__img" src="images/p02-middle.jpg" alt="Image"/>
            </div>
        </div>
        <div class="grid__item-caption">
            <h3 class="grid__item-title"></h3>
        </div>
    </a>	
</div>

<div class="grid grid--effect-vega">
    <a href="#" class="grid__item grid__item--c3">
        <div class="stack">
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__deco"></div>
            <div class="stack__figure">
                <img class="stack__img" src="images/p03-middle.jpg" alt="Image"/>
            </div>
        </div>
        <div class="grid__item-caption">
            <h3 class="grid__item-title"></h3>
        </div>
    </a>	
</div>
<!--~~~~~~~~~~~~~~~~~~--> 
```
