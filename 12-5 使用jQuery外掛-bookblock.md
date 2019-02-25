# 12-5 使用jQuery外掛-bookblock

### 練習重點
```
使用jQuery外掛, 增加網頁特殊功能.
```

### 執行結果:
![GitHub Logo](/imgs/results12-5.jpg)


### 外掛網址
```
https://github.com/codrops/BookBlock
```

### 引用官網外掛檔案
```
   |__ <dist>
         |__ <css>
         |     |__ bookblock.css
         |     |__ demo1.css 
         |      
         |__ <js>
         |      |__ jquery.bookblock.js
         |      |__ jquerypp.custom.js      
         |      |__ modernizer.custom.js          
         |
         |__ <fonts> (資料夾及其中檔案)
```


### 檔案放置方式(以11-3範例為基礎, 增修以下):
```
   |__ index.html  (引用外掛, 增加顯示區域) 
   |  
   |__ <fonts>  (由官網複製)  
   |
   |__ <imgs>
   |     |__ p01-book.jpg   (600像素*400像素)
   |     |__ p01-book.jpg   (600像素*400像素)
   |     |__ p01-book.jpg   (600像素*400像素)
   |     |__ p01-book.jpg   (600像素*400像素)
   |
   |__ <css>
   |     |__ bookblock.css     (由官網複製) 
   |     |__ demo1.css         (由官網複製) 
   |     |__ my.bookblock.css  (自行增加)    
   |
   |__ <js>
         |__ jquery.bookblock.js     (由官網複製)     
         |__ jquerypp.custom.js      (由官網複製)  
         |__ modernizer.custom.js    (由官網複製)           
         |__ my.jquery.bookblock.js  (自行增加)       
```


### (1) my.bookblock.css
``` css
@charset "utf-8";

.bb-bookblock {	
    width: 600px;
    height: 400px;
    z-index: 15;
}

.bb-custom-wrapper {
    width: 600px;
}

.bb-custom-wrapper nav a {
    background:#1F2FC2;
    color: #ff0;
}
```

### (2) my.jquery.bookblock.js
``` js
var Page = (function() {
    var config = {
        $bookBlock : $( '#bb-bookblock' ),
        $navNext : $( '#bb-nav-next' ),
        $navPrev : $( '#bb-nav-prev' ),
        $navFirst : $( '#bb-nav-first' ),
        $navLast : $( '#bb-nav-last' )
    },
    
    init = function() {
        config.$bookBlock.bookblock( {
            speed : 800,
            shadowSides : 0.8,
            shadowFlip : 0.7
        });
        initEvents();
    },
		
    initEvents = function() {			
        var $slides = config.$bookBlock.children();

        // add navigation events
        config.$navNext.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'next' );
            return false;
        });

        config.$navPrev.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'prev' );
            return false;
        });

        config.$navFirst.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'first' );
            return false;
        });

        config.$navLast.on( 'click touchstart', function() {
            config.$bookBlock.bookblock( 'last' );
            return false;
        });
			
        // add swipe events
        $slides.on( {
            'swipeleft' : function( event ) {
                config.$bookBlock.bookblock( 'next' );
                return false;
            },
            'swiperight' : function( event ) {
                config.$bookBlock.bookblock( 'prev' );
                return false;
            }
        });

        // add keyboard events
        $( document ).keydown( function(e) {
            var keyCode = e.keyCode || e.which;
            var arrow = {
                left : 37,
                up : 38,
                right : 39,
                down : 40
            };

            switch (keyCode) {
                case arrow.left:
                    config.$bookBlock.bookblock( 'prev' );
                    break;
                case arrow.right:
                    config.$bookBlock.bookblock( 'next' );
                    break;
            }
        });
    };
    return { init : init };
})();


$(function(){
    Page.init();
});
```


### (3) index.html (引用外掛)  
``` html
.
.
(加入css)
<link href="css/bookblock.css" rel="stylesheet" />
<link href="css/demo1.css" rel="stylesheet" />
<link href="css/my.bookblock.css" rel="stylesheet" />
.
.
.
.
(加入js)
<script src="js/modernizr.custom.js"></script>    
<script src="js/jquerypp.custom.js"></script>     
<script src="js/jquery.bookblock.js"></script>  
<script src="js/my.jquery.bookblock.js"></script>  
.
.
```

### (4) index.html (增加顯示區域)  
``` html
<!--~~~~~~~~~~~~~~~~~-->
<!-- bookblock 測試  -->
<!--~~~~~~~~~~~~~~~~~-->
<p>    
    <div class="main clearfix">
        <div class="bb-custom-wrapper">                        
            <div id="bb-bookblock" class="bb-bookblock">
                <div class="bb-item">
                    <a href="#"><img src="imgs/p01-book.jpg" alt="p01"/></a>
                </div>
                <div class="bb-item">
                    <a href="#"><img src="imgs/p02-book.jpg" alt="p02"/></a>
                </div>
                <div class="bb-item">
                    <a href="#"><img src="imgs/p03-book.jpg" alt="p03"/></a>
                </div>
                <div class="bb-item">
                    <a href="#"><img src="imgs/p04-book.jpg" alt="p04"/></a>
                </div>
            </div>
            <nav>
                <a id="bb-nav-first" href="#" class="bb-custom-icon bb-custom-icon-first">First page</a>
                <a id="bb-nav-prev" href="#" class="bb-custom-icon bb-custom-icon-arrow-left">Previous</a>
                <a id="bb-nav-next" href="#" class="bb-custom-icon bb-custom-icon-arrow-right">Next</a>
                <a id="bb-nav-last" href="#" class="bb-custom-icon bb-custom-icon-last">Last page</a>
            </nav>
        </div>
    </div>
</p>
<!--~~~~~~~~~~~~~~~~~--> 
```
